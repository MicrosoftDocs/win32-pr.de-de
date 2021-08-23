---
description: Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungssteuerfeld in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Erstellen der Benutzeroberfläche für die Kennworteingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b558243e24e4977d8e28311ac7643c118a26cdf62c89366694a16227b30c1969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066070"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Erstellen der Benutzeroberfläche für die Kennworteingabe

Fügen Sie für jedes Kennwort, das vom Benutzer eingegeben werden muss, ein Bearbeitungssteuerfeld in einem Dialogfeld hinzu, in dem der Wert des Kennworts in einer Eigenschaft gespeichert wird. Dieses [Bearbeitungssteuer](edit-control.md) steuerelement sollte über das [Kennwortsteuerungsattribut verfügen.](password-control-attribute.md) Dies gibt an, dass die eingegebene Eigenschaft ein Kennwort ist und verhindert, dass das Installationsprogramm die Eigenschaft in die Protokolldatei schreibt.

Die [](control-attributes.md) Steuerelementattribute für das Steuerelement zur Kennwortbearbeitung sind msidbControlAttributesVisible, msidbControlAttributesEnabled und msidbControlAttributesPasswordInput (1 + 2 + 2097152). X, Y, Width, Height und Control Next hängen vom Layout des Steuerelements \_ im Dialogfeld ab.

[Steuertabelle](control-table.md)



| Dialog\_ | Steuerelement\_            | type | X   | J   | Breite | Höhe | Attribute | Eigenschaft         | Text | Weiter \_ steuern | Hilfe |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Bearbeiten | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Abbrechen        |      |



 

Fahren Sie mit [Sichern der Installation fort.](securing-the-installation.md)

 

 



