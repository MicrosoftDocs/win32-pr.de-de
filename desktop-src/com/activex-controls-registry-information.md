---
title: ActiveX Steuert Registrierungsinformationen
description: ActiveX Steuert Registrierungsinformationen
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f062c11304c50161308cc5c6e43001c23f63486e60e568f61d6335f0947380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737384"
---
# <a name="activex-controls-registry-information"></a>ActiveX Steuert Registrierungsinformationen

Es werden eine Reihe von Registrierungseinträgen und -flags verwendet. Darüber hinaus können Steuerelemente Komponentenkategorien unterstützen, um die features zu klassifizieren, die sie bereitstellen.

Registrierungsschlüssel im Zusammenhang mit Steuerelementen werden in der folgenden Struktur mit einem Sternchen markiert:

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

Der **DefaultIcon-Eintrag** wird verwendet, um ein Symbol zu identifizieren, das angezeigt werden soll, wenn das Steuerelement auf ein Symbol minimiert wird. Die [**ExtractIcon-Funktion**](/windows/win32/api/shellapi/nf-shellapi-extracticona) wird verwendet, um das Symbol aus dem angegebenen .DLL oder .EXE zu erhalten.

Der **Eintrag ToolboxBitmap32** identifiziert den Modulnamen und den Ressourcenbezeichner für eine 16 15-Bitmap, die für das Gesicht einer Symbolleiste oder \* Toolboxschaltfläche verwendet werden soll. Die Standardgröße Windows symbol ist zu groß, um für diesen Zweck verwendet zu werden. Dieser Eintrag unterstützt speziell Steuerelementcontainer mit einem Entwurfsmodus, in dem Steuerelemente ausgewählt und auf einem zu entwerfenden Formular platziert werden. Beispielsweise wird in Visual Basic das Symbol des Steuerelements im Entwurfsmodus in der toolbox Visual Basic angezeigt.

Der **Control-Eintrag** markiert ein Objekt als -Steuerelement. Dieser Eintrag wird häufig von Containern verwendet, um Dialogfelder zu füllen. Der Container verwendet diesen Unterschlüssel, um zu bestimmen, ob ein Objekt in ein Dialogfeld mit Steuerelementen enthalten sein soll.

Der **Insertable-Unterschlüssel** kann auch mit Steuerelementen verwendet werden, je nachdem, ob das Objekt nur als eingebettetes Objekt ohne spezielle Steuerelementfeatures fungieren kann. Mit **Insertable markierte** Objekte werden im Dialogfeld Objekt einfügen ihres Containers angezeigt. Der **Insertable-Eintrag** bedeutet in der Regel, dass das Steuerelement mit Containern ohne Steuerung getestet wurde.

Sowohl die **Unterschlüssel Insertable** als **auch control** sind optional. Ein Steuerelement kann  den Einfügebaren Unterschlüssel weglassen, wenn es nicht für die Arbeit mit älteren Containern konzipiert ist, die Steuerelemente nicht verstehen. Ein Steuerelement kann  die Steuerungsschlüssel weglassen, wenn es nur für die Arbeit mit einem bestimmten Container konzipiert ist und daher nicht in andere Container eingefügt werden soll.

Steuerelemente sollten über ein Properties-Verb, OLEIVERB PROPERTIES, sowie \_ alle anderen Verben verfügen, die sie unterstützen. Das Properties-Verb sowie das Standardverb OLEIVERB PRIMARY weisen das Steuerelement \_ an, sein Eigenschaftenblatt anzuzeigen. Das Verb Eigenschaften wird als Eigenschaftenelement im Menü des Containers angezeigt, wenn das Steuerelement aktiv ist. Auf diese Weise kann das Steuerelement eine eigene Eigenschaftenseite anzeigen, die dem Endbenutzer einige nützliche Funktionen ermöglicht, auch wenn der Container keine Steuerelemente verarbeitet.

Ein Steuerelement definiert den **MiscStatus-Schlüssel,** um sich selbst für potenzielle Container zu beschreiben. Die Bits übernehmen die Werte von [**OLEMISC,**](/windows/win32/api/oleidl/ne-oleidl-olemisc)und -Steuerelemente fügen dieser Enumeration mehrere Werte hinzu. Weitere Informationen **finden Sie unter OLEMISC-Enumerationswerte.** Der Client kann diese Informationen abrufen, indem er [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) aufruft, ohne das Steuerelement zuerst instanziieren zu müssen.

Schließlich beschreibt **Version** die Version des Steuerelements, die mit der Version der Typbibliothek übereinstimmen sollte, die diesem Steuerelement zugeordnet ist.

Außerdem markiert das Attributsteuerzeichen in den Typinformationen für ein Steuerelement einen Co-Klasse-Eintrag als Beschreibung eines Steuerelements.

 

 