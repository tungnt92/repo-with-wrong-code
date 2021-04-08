# Changelog

<% if(version && (version.name || version.number)) { %>##<% if(version.name){%> <%= version.name %><% } %> <%= version.number %> <% if(version.date){ %>( <%= version.date %> )<% } %><%= '\n' %><% } %>
<% _.forEach(sections, function(section){
if(section.commitsCount > 0) { %>
## <%= section.title %>
<% _.forEach(section.commits, function(commit){ %>  - <%= printCommit(commit) %><% }) %>
<% _.forEach(section.components, function(component){ %>  - **<%= component.name %>**
<% _.forEach(component.commits, function(commit){ %>    - <%= printCommit(commit) %><% }) %>
<% }) %>
<% } %>
<% }) %>

---
