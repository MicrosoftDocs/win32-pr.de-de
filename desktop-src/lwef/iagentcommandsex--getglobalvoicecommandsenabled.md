---
title: Iagentcommandsex getglobalvoicecommandsenabled
description: Iagentcommandsex getglobalvoicecommandsenabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390238"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>Iagentcommandsex:: getglobalvoicecommandsenabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Ruft ab, ob die Sprachgrammatik für die globalen Befehle des Agents aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*
</dt> <dd>

Die Adresse, die **true** erhält, wenn die Sprachgrammatik für die globalen Befehle des Agents aktiviert ist, andernfalls **false** .

</dd> </dl>

Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu. Wenn diese Methode **false** zurückgibt, sind alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte anderer Clients nicht in der Grammatik enthalten. Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen. Diese Einstellung gibt jedoch nicht an, wie diese Befehle in das Popup Menü des Zeichens eingefügt werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: setglobalvoicecommandsenabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 