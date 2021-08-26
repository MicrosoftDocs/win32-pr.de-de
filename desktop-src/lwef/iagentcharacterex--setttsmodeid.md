---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24195fd177abbde3c6423f966df67ba0faeaf315038d7f8cb0b4ca136f16c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114720"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Legt die Modus-ID des TTS-Engine-Satzes für das Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

Die Modus-ID-Einstellung der TTS-Engine für das Zeichen.

> [!Note]  
> **IAgentCharacterEx:SetTTSModeID** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht mit der TTS-Moduseinstellung des kompilierten Zeichens übereinstimmt.

 

</dd> </dl>

Diese Einstellung bestimmt den bevorzugten Engine-Modus für die gesprochene TTS-Ausgabe eines Zeichens. Die Modus-ID für eine TTS-Engine (Text-to-Speech) ist die vom Sprachanbieter definierte GUID, die den Modus der Engine eindeutig identifiziert (formatiert mit geschweiften Klammern und Bindestrichen). Weitere Informationen finden Sie in der Dokumentation zum [Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx)

Wenn Sie eine TTS-Modus-ID festlegen, überschreibt sie den Serverversuch, eine Sprach-Engine basierend auf der kompilierten TTS-Modus-ID des Zeichens, der aktuellen Systemsprach-ID und der aktuellen Sprach-ID des Zeichens abzugleichen. Wenn Sie jedoch versuchen, eine Modus-ID festzulegen, wenn der Benutzer die Sprachausgabe im Eigenschaftenblatt des Microsoft-Agents deaktiviert hat oder wenn die zugeordnete Engine nicht installiert ist, tritt bei diesem Aufruf ein Fehler auf.

Wenn Sie keine TTS-Engine-Modus-ID für das Zeichen festlegen, legt der Server eine Engine fest, die der Spracheinstellung des Zeichens entspricht (mithilfe von Microsoft Speech-API-Schnittstellen). Wenn Sie diese Eigenschaft festlegen, wird die zugeordnete Engine geladen, wenn sie noch nicht geladen wurde.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Anforderungen der Sprach-Engine des Microsoft-Agents basieren auf der Microsoft Speech-API. Engines, die die SAPI-Anforderungen des Microsoft-Agents unterstützen, können installiert und mit dem Agent verwendet werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




