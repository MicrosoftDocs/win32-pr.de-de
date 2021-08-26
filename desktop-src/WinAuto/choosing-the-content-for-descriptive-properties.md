---
title: Auswählen des Inhalts für beschreibende Eigenschaften
description: Während der Inhalt einiger Eigenschaften spezifisch ist, besteht der Inhalt für andere Eigenschaften aus beschreibendem Text, der dem Serverentwickler zur Verfügung steht.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5215a6592d11272223654184340c4df8b299b88edb5b5f4addbd2c8d4712ab74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071850"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Auswählen des Inhalts für beschreibende Eigenschaften

Während der Inhalt einiger Eigenschaften spezifisch ist, besteht der Inhalt für andere Eigenschaften aus beschreibendem Text, der dem Serverentwickler zur Verfügung steht. Darüber hinaus variiert der Informationstyp für jede Eigenschaft je nach Objekt. Die folgende Tabelle enthält Vorschläge für die Auswahl des Inhalts dieser beschreibenden Eigenschaften.



| Eigenschaft                                        | Inhaltsvorschläge                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name**](name-property.md)                   | Eine Bezeichnung, die das Objekt in seinem Container kurz beschreibt und identifiziert, z. B. den Text in einer Pushschaltfläche, den Namen eines Menüelements oder eine Bezeichnung, die neben einem Bearbeitungssteuerelement angezeigt wird.                                                                              |
| [**Defaultaction**](defaultaction-property.md) | Die Standardinteraktion mit dem -Objekt. Die von dieser Eigenschaft zurückgegebene Zeichenfolge ist entweder ein einzelnes Verb, z. B. "Press" für eine Symbolleistenschaltfläche, oder ein kurzer Ausdruck, der mit einem Verb beginnt.                                                                               |
| [**Wert**](value-property.md)                 | Informationen, die im -Objekt enthalten sind, z. B. der Text in einem Bearbeitungssteuerelement oder der Dateiname eines HTML-Links. Der Inhalt der [**Value-Eigenschaft**](value-property.md) kann sich ändern, während sich der Inhalt der [**Name-Eigenschaft**](name-property.md) nicht ändert. |
| [**Beschreibung**](description-property.md)     | Beschreibt die Darstellung des Objekts.                                                                                                                                                                                                                                    |
| [**Hilfe**](help-property.md)                   | Informationen im QuickInfo- oder Sprechblasenstil, die verwendet werden, um zu beschreiben, was das Objekt tut oder wie es verwendet wird.                                                                                                                                                                   |
| [**Helptopic**](helptopic-property.md)         | Ein Kontextbezeichner eines [WinHelp-Themas,](/windows/win32/api/winuser/nf-winuser-winhelpa) das das Objekt dokumentiert.                                                                                                                                                 |



 

Verwenden Sie einen der vordefinierten [Objektrollenwerte](object-roles.md) für die [**Rolle**](role-property.md) und die entsprechende Kombination von [Objektzustandskonstanten](object-state-constants.md) für den [**Zustand**](state-property.md).

Der Inhalt der Eigenschaften für benutzerdefinierte Steuerelemente muss mit dem Inhalt der Eigenschaften für die vom System bereitgestellten Steuerelemente übereinstimmen, die die benutzerdefinierten Steuerelemente emulieren. Informationen zu den Eigenschaften, die von vom System bereitgestellten Steuerelementen unterstützt werden, finden Sie unter [Anhang A: Unterstützte Benutzeroberfläche Elements Reference](appendix-a--supported-user-interface-elements-reference.md).

 

 