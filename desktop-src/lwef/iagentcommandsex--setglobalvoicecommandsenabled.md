---
title: Iagentcommandsex setglobalvoicecommandsenabled
description: Iagentcommandsex setglobalvoicecommandsenabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101562"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>Iagentcommandsex:: setglobalvoicecommandsenabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Legt die [**aktivierte**](enabled-property.md) Eigenschaft für die Sprachgrammatik der globalen Befehle des Microsoft-Agents fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*benabel*
</dt> <dd>

Ein boolescher Wert, der festlegt, ob die Sprachgrammatik der globalen Befehle des Agents aktiviert ist. **True** aktiviert die Sprachgrammatik; **False** deaktiviert es.

</dd> </dl>

Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu. Wenn diese Einstellung auf " **false**" festgelegt ist, deaktiviert der-Agent alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte anderer Clients. Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen. Da dadurch jedoch möglicherweise der sprach Zugriff auf andere Clients blockiert wird, setzen Sie diese Eigenschaft nach dem Verarbeiten der Spracheingabe des Benutzers auf " **true** " zurück.

Das Deaktivieren der Eigenschaft wirkt sich nicht auf das Popup Menü des Zeichens aus. Die vom Server hinzugefügten globalen Befehle werden weiterhin angezeigt. Sie können Sie nicht aus dem Popupmenü entfernen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: getglobalvoicecommandsenabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 