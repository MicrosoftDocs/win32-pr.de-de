---
title: ActiveX steuert Registrierungsinformationen
description: ActiveX steuert Registrierungsinformationen
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517138"
---
# <a name="activex-controls-registry-information"></a>ActiveX steuert Registrierungsinformationen

Es gibt eine Reihe von Registrierungs Einträgen und Flags, die verwendet werden. Darüber hinaus können Steuerelemente Komponenten Kategorien zum Klassifizieren der Features unterstützen, die Sie bereitstellen.

Registrierungsschlüssel, die sich auf Steuerelemente beziehen, werden mit einem Sternchen in der folgenden Struktur markiert:

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

Der **DefaultIcon** -Eintrag wird zum Identifizieren eines Symbols verwendet, das angezeigt wird, wenn das Steuerelement auf ein Symbol minimiert wird. Die [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) -Funktion wird verwendet, um das Symbol aus der zu erhalten. DLL oder. Die exe-Datei wurde angegeben.

Der **ToolboxBitmap32** -Eintrag identifiziert den Modulnamen und den Ressourcen Bezeichner für eine 16 \* 15-Bitmap, die für das Gesicht einer Symbolleiste oder Toolbox Schaltfläche verwendet werden soll. Die standardmäßige Windows-Symbolgröße ist zu groß, um für diesen Zweck verwendet zu werden. Dieser Eintrag unterstützt speziell Steuerelement Container mit einem Entwurfs Modus, in dem ein Steuerelement ausgewählt und in einem entworfenen Formular platziert wird. Beispielsweise wird in Visual Basic das Symbol des-Steuer Elements im Entwurfs Modus in der Visual Basic Toolbox angezeigt.

Der **Steuer** Element Eintrag kennzeichnet ein Objekt als-Steuerelement. Dieser Eintrag wird häufig von Containern verwendet, um Dialogfelder auszufüllen. Der Container verwendet diesen Unterschlüssel, um zu bestimmen, ob ein Objekt in ein Dialogfeld aufgenommen werden soll, in dem Steuerelemente angezeigt werden.

Der **Insertable** -Unterschlüssel kann auch mit-Steuerelementen verwendet werden, je nachdem, ob das Objekt nur als direktes eingebettetes Objekt ohne spezielle Steuerelement Funktionen fungieren kann. Objekte, die mit **Insertable** gekennzeichnet sind, werden im Dialogfeld Objekt einfügen ihres Containers angezeigt. Der **Insertable** -Eintrag bedeutet im Allgemeinen, dass das Steuerelement mit nicht-Steuerungs Containern getestet wurde.

Die Unterschlüssel **Insertable** und **Control** sind optional. Ein Steuerelement kann den Unterschlüssel **Insertable** weglassen, wenn er nicht für die Arbeit mit älteren Containern konzipiert ist, die Steuerelemente nicht verstehen. Ein Steuerelement kann die **Steuer** Element Taste weglassen, wenn es nur für den Einsatz mit einem bestimmten Container konzipiert ist und daher nicht in andere Container eingefügt werden soll.

Steuerelemente sollten über ein Eigenschaften Verb, oleiverb- \_ Eigenschaften und alle anderen Verben verfügen, die Sie unterstützen. Das Eigenschaften Verb sowie das Standard-Verb oleiverb Primary weisen das-Steuerelement an, das zugehörige Eigenschaften \_ Blatt anzuzeigen. Das Eigenschaften-Verb wird im Menü des Containers als Eigenschaften Element angezeigt, wenn das Steuerelement aktiv ist. Auf diese Weise kann das Steuerelement eine eigene Eigenschaften Seite anzeigen, die dem Endbenutzer nützliche Funktionen bietet, auch wenn der Container keine Steuerelemente behandelt.

Ein-Steuerelement definiert den **fehlstatus** -Schlüssel, um sich für potenzielle Container zu beschreiben. Die Bits übernehmen die Werte aus [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), und die Steuerelemente fügen dieser Enumeration mehrere Werte hinzu. Weitere Informationen finden Sie in den **OLEMISC** -Enumerationswerten. Der Client kann diese Informationen durch Aufrufen von [**IOleObject:: getfehlstatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) abrufen, ohne das Steuerelement zuerst instanziieren zu müssen.

Schließlich wird in **Version** die Version des-Steuer Elements beschrieben, die mit der Version der Typbibliothek, die diesem Steuerelement zugeordnet ist, entsprechen sollte.

Auch in den Typinformationen für ein Steuerelement markiert das Attribut Steuerelement einen Co-Klassen Eintrag als Beschreibung eines Steuer Elements.

 

 