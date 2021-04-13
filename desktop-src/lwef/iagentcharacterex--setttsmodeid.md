---
title: Iagentcharakteriex settungmodeid
description: Iagentcharakteriex settungmodeid
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389978"
---
# <a name="iagentcharacterexsetttsmodeid"></a>Iagentcharakteriex:: settungmodeid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Legt die Mode-ID des TTS-Engine-Satzes für das Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszmodeid*
</dt> <dd>

Die Modus-ID-Einstellung der TTS-Engine für das Zeichen.

> [!Note]  
> **Iagentcharakteriex: setttmodeid** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht der kompilierten TTS-Moduseinstellung des Zeichens entspricht.

 

</dd> </dl>

Diese Einstellung bestimmt den bevorzugten Engine-Modus für die gesprochene TTS-Ausgabe eines Zeichens. Die Mode-ID für eine TTS-Engine (Text-to-Speech) ist die GUID, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert (mit geschweiften Klammern und Bindestrichen formatiert). Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).

Wenn Sie eine TTS-Modus-ID festlegen, überschreibt Sie den Server Versuch, eine Sprach-Engine auf Grundlage der kompilierten TTS-Modus-ID des Zeichens, der aktuellen Systemsprachen-ID und der aktuellen Sprach-ID des Zeichens abzugleichen. Wenn Sie jedoch versuchen, eine Modus-ID festzulegen, wenn der Benutzer die Sprachausgabe auf der Eigenschaften Seite des Microsoft-Agents deaktiviert hat oder wenn das zugehörige Modul nicht installiert ist, tritt bei diesem Vorgang ein Fehler auf.

Wenn Sie keine ID des TTS-Engine-Modus für das Zeichen festlegen, legt der Server ein Modul fest, das mit der Spracheinstellung des Zeichens (über Microsoft Speech API-Schnittstellen) übereinstimmt. Wenn Sie diese Eigenschaft festlegen, wird die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex: getttmodeid**](iagentcharacterex--getttsmodeid.md)


 

 




