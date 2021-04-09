---
title: Iagentcharakteriex getttmodeid
description: Iagentcharakteriex getttmodeid
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038633"
---
# <a name="iagentcharacterexgetttsmodeid"></a>Iagentcharakteriex:: getttmodeid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Ruft die Modus-ID des TTS-Engine-Satzes für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszmodeid*
</dt> <dd>

Adresse eines BSTR, der die Modus-ID-Einstellung der TTS-Engine für das Zeichen empfängt.

</dd> </dl>

Diese Einstellung gibt die ID des TTS (Text-zu-Sprache-Engine) für die gesprochene Ausgabe eines Zeichens zurück. Die Mode-ID für eine TTS-Engine ist eine Zeichen folgen Darstellung der GUID (mit geschweiften Klammern und Bindestrichen formatiert), die durch den Sprachanbieter definiert wird, der die Engine eindeutig identifiziert. Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx). Wenn Sie diese Eigenschaft Abfragen, wird die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist.

Wenn Sie keine ID des TTS-Engine-Modus für das Zeichen festlegen, versucht der Server, eine Engine zurückzugeben, die (über Microsoft Speech API-Schnittstellen) die kompilierte TTS-Einstellung des Zeichens und die aktuelle Spracheinstellung des Zeichens abgleicht. Wenn diese unterschiedlich sind, wird die Einstellung für den erstellten Modus durch die Spracheinstellung des Zeichens überschrieben. Wenn Sie die Spracheinstellung des Zeichens nicht festgelegt haben, ist die Sprache des Zeichens die Standardsprachen-ID des Benutzers, und der Server versucht, die Entsprechung basierend auf dieser Sprach-ID zu erhalten.

Diese Funktion schlägt fehl, wenn [**iagentaudioobjectproperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) **false** zurückgibt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: settungmodeid**](iagentcharacterex--setttsmodeid.md)


 

 




