---
description: Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungs Steuerelement in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349810"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe

Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungs Steuerelement in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird. Dieses [Bearbeitungs Steuer](edit-control.md) Element muss über das [Attribut "Password Control](password-control-attribute.md)" verfügen. Dies gibt an, dass die eingegebene Eigenschaft ein Kennwort ist und verhindert, dass das Installationsprogramm die Eigenschaft in die Protokolldatei schreibt.

Die [Steuerelement Attribute](control-attributes.md) für das Kenn Wort Bearbeitungs Steuerelement sind msidbcontrolattributesvisible, msidbcontrolattributesaktiviertes und msidbcontrolattributespasswordinput (1 + 2 + 2097152). "X", "Y", "width", "Height" und "Control \_ Next" hängen vom Layout des Steuer Elements im Dialogfeld ab.

[Steuerungs Tabelle](control-table.md)



| Dialog\_ | Steuerelement\_            | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft         | Text | Nächstes Steuerelement \_ | Hilfe |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | Testuserpasswordebug | Bearbeiten | 25  | 120 | 300   | 20     | 2097155    | Testuserpassword |      | Abbrechen        |      |



 

Fahren Sie mit [dem Sichern der Installation](securing-the-installation.md)fort.

 

 



