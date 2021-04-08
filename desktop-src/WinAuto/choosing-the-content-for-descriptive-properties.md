---
title: Auswählen des Inhalts für beschreibende Eigenschaften
description: Während der Inhalt einiger Eigenschaften spezifisch ist, besteht der Inhalt für andere Eigenschaften aus beschreibenden Text, der dem Server Entwickler zur Verfügung gestellt wird.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729961"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Auswählen des Inhalts für beschreibende Eigenschaften

Während der Inhalt einiger Eigenschaften spezifisch ist, besteht der Inhalt für andere Eigenschaften aus beschreibenden Text, der dem Server Entwickler zur Verfügung gestellt wird. Außerdem variiert der Typ der Informationen für jede Eigenschaft je nach Objekt. In der folgenden Tabelle finden Sie Vorschläge zur Auswahl des Inhalts dieser beschreibenden Eigenschaften.



| Eigenschaft                                        | Inhalts Vorschlag                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name**](name-property.md)                   | Eine Bezeichnung, die das Objekt innerhalb des Containers kurz beschreibt und identifiziert, z. b. den Text in einer Schaltfläche "Push", den Namen eines Menü Elements oder eine Bezeichnung, die neben einem Bearbeitungs Steuerelement angezeigt wird.                                                                              |
| [**DEFAULTACTION**](defaultaction-property.md) | Die Standard Interaktion mit dem-Objekt. Die von dieser Eigenschaft zurückgegebene Zeichenfolge ist entweder ein einzelnes Verb, z. b. "drücken" für eine Symbolleisten-Schaltfläche oder ein kurzer Ausdruck, der mit einem Verb beginnt.                                                                               |
| [**Wert**](value-property.md)                 | Informationen, die im-Objekt enthalten sind, z. b. der Text in einem Bearbeitungs Steuerelement oder der Dateiname eines HTML-Links. Der Inhalt der [**value**](value-property.md) -Eigenschaft kann sich ändern, während der Inhalt der [**Name**](name-property.md) -Eigenschaft nicht geändert wird. |
| [**Beschreibung**](description-property.md)     | Beschreibt die Darstellung des Objekts.                                                                                                                                                                                                                                    |
| [**Hilfe**](help-property.md)                   | Informationen zur QuickInfo-oder Sprechblasen Formatierung werden verwendet, um zu beschreiben, was das Objekt tut oder wie es verwendet wird.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Ein Kontext Bezeichner eines [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) -Themas, das das Objekt dokumentiert.                                                                                                                                                 |



 

Verwenden Sie einen der vordefinierten [Objekt Rollen](object-roles.md) Werte für die [**Rolle**](role-property.md) und die geeignete Kombination von [Objekt Zustands Konstanten](object-state-constants.md) für den [**Zustand**](state-property.md).

Der Inhalt der Eigenschaften für benutzerdefinierte Steuerelemente muss dem Inhalt der Eigenschaften für die vom System bereitgestellten Steuerelemente entsprechen, die von den benutzerdefinierten Steuerelementen emuliert werden. Informationen zu den Eigenschaften, die von vom System bereitgestellten Steuerelementen unterstützt werden, finden Sie [unter Anhang A: Unterstützte Benutzeroberflächen Elemente](appendix-a--supported-user-interface-elements-reference.md).

 

 