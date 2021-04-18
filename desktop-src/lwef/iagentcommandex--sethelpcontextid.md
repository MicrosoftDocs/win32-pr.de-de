---
title: Iagentcommandex-elementpcontextid
description: Iagentcommandex-elementpcontextid
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338060"
---
# <a name="iagentcommandexsethelpcontextid"></a>Iagentcommandex:: Setup Element-ID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Legt die [**HelpContextID**](helpcontextid-property-com.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*"ulid"*
</dt> <dd>

Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und diese in der [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben. Der Microsoft-Agent ruft automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt. Wenn in [**HelpContextID**](helpcontextid-property-com.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandex:: gethelpcontextid**](iagentcommandex--gethelpcontextid.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name


 

 