---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e6bc029a6fce1da3d6f920a25ccc86c49619751a6bd43f865154bd7a235696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105488"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Ruft die Modus-ID des TTS-Engine-Satzes für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Adresse eines BSTR, der die Modus-ID-Einstellung der TTS-Engine für das Zeichen empfängt.

</dd> </dl>

Diese Einstellung gibt die TTS-Engine-Modus-ID (Text-to-Speech) für die gesprochene Ausgabe eines Zeichens zurück. Die Modus-ID für eine TTS-Engine ist eine Zeichenfolgendarstellung der GUID (formatiert mit geschweiften Klammern und Bindestrichen), die vom Sprachanbieter definiert wird, der die Engine eindeutig identifiziert. Weitere Informationen finden Sie in der Dokumentation zum [Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx) Wenn Sie diese Eigenschaft abfragen, wird die zugeordnete Engine geladen, wenn sie noch nicht geladen wurde.

Wenn Sie keine TTS-Engine-Modus-ID für das Zeichen festlegen, versucht der Server, eine Engine zurückzugeben, die der kompilierten TTS-Einstellung des Zeichens und der aktuellen Spracheinstellung des Zeichens entspricht (mithilfe von Microsoft Speech-API-Schnittstellen). Wenn diese unterschiedlich sind, überschreibt die Spracheinstellung des Zeichens seine Einstellung für den erstellungsmodus. Wenn Sie die Spracheinstellung des Zeichens nicht festgelegt haben, ist die Sprache des Zeichens die Standardsprach-ID des Benutzers, und der Server versucht die Übereinstimmung basierend auf dieser Sprach-ID.

Diese Funktion schlägt nicht fehl, wenn [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) **False** zurückgibt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Anforderungen der Sprach-Engine des Microsoft-Agents basieren auf der Microsoft Speech-API. Engines, die die SAPI-Anforderungen des Microsoft-Agents unterstützen, können installiert und mit dem Agent verwendet werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




