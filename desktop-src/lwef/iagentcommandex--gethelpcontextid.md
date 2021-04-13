---
title: Iagentcommandex gethelpcontextid
description: Iagentcommandex gethelpcontextid
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390294"
---
# <a name="iagentcommandexgethelpcontextid"></a>Iagentcommandex:: gethelpcontextid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Ruft die [**HelpContextID**](helpcontextid-property-com.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulid*
</dt> <dd>

Adresse einer Variablen, die die Kontext Nummer des Hilfe Themas empfängt, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft Ihres Zeichens auf diese Datei festgelegt haben, ruft der Microsoft-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt. Wenn in [**HelpContextID**](helpcontextid-property-com.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandex::**](iagentcommandex--sethelpcontextid.md)Setup Element-ID, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name


 

 