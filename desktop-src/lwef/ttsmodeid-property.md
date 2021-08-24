---
title: TTSModeID-Eigenschaft
description: TTSModeID-Eigenschaft
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a720b06362b77418434669146a0d89dea8afd37d7a44c4079b2e12c24fcd2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607960"
---
# <a name="ttsmodeid-property"></a>TTSModeID-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den TTS-Engine-Modus zurück, der für das Zeichen verwendet wird, oder legt den TTS-Engine-Modus fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). TTSModeID_ *  \[  =  *ModeID*\]



| Teil     | Beschreibung                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Ein Zeichenfolgenausdruck, der der Modus-ID einer Sprach-Engine entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Eigenschaft bestimmt die TTS-Engine-Modus-ID (Text-to-Speech) für die gesprochene Ausgabe eines Zeichens. Die Modus-ID für eine TTS-Engine ist eine formatierte Zeichenfolge, die vom Sprachanbieter definiert wird und den Modus der Engine eindeutig identifiziert. Weitere Informationen finden Sie unter [Zugreifen auf eine Sprach-Engine in Ihrem Code.](accessing-a-speech-engine-in-your-code.md)

Das Festlegen dieser Eigenschaft überschreibt den Versuch des Servers, eine Engine basierend auf der kompilierten TTS-Einstellung des Zeichens und der aktuellen [**LanguageID-Einstellung**](languageid-property.md) des Zeichens zu laden. Wenn Sie jedoch eine Modus-ID für eine Engine angeben, die nicht installiert ist, oder wenn der Benutzer die Sprachausgabe im Eigenschaftenblatt des Microsoft-Agents deaktiviert hat (**AudioOutput.Enabled = False**), löst der Server einen Fehler aus.

Wenn Sie nicht (oder nicht erfolgreich) eine TTS-Modus-ID für das Zeichen festgelegt haben, überprüft der Server, ob die kompilierte TTS-Moduseinstellung des Zeichens mit der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens übereinstimmt und ob die zugeordnete TTS-Engine installiert ist. Wenn ja, gibt der TTS-Modus, der vom Zeichen für die gesprochene Ausgabe verwendet wird, und diese Eigenschaft diese Modus-ID zurück. Andernfalls fordert der Server eine kompatible SAPI-Sprach-Engine an, die der **LanguageID** des Zeichens entspricht, sowie das Geschlecht und das Alter, das für die ID des kompilierten Modus des Zeichens festgelegt ist. Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, ist die **LanguageID** die aktuelle Benutzersprache. Wenn keine übereinstimmende Engine gefunden wird, gibt die Abfrage dieser Eigenschaft eine leere Zeichenfolge für die Modus-ID der Engine zurück. Wenn Sie diese Eigenschaft abfragen, wenn der Benutzer die Sprachausgabe im Eigenschaftenblatt des Microsoft-Agents deaktiviert hat **(AudioOutput.Enabled = False),** ist der Wert eine leere Zeichenfolge.

Wenn Sie diese Eigenschaft abfragen oder festlegen, wird die zugeordnete Engine geladen (sofern sie noch nicht geladen ist). Wenn jedoch die in der kompilierten TTS-Einstellung des Zeichens angegebene Engine installiert ist und mit der Sprach-ID-Einstellung des Zeichens übereinstimmt, wird die Engine geladen, wenn das Zeichen geladen wird.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Anforderungen der Sprach-Engine des Microsoft-Agents basieren auf der Microsoft Speech-API. Engines, die die SAPI-Anforderungen des Microsoft-Agents unterstützen, können installiert und mit dem -Agent verwendet werden.

> [!Note]  
> Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf Ihrem System keine kompatible Soundunterstützung installiert ist.

 

> [!Note]  
> Das Festlegen der **TTSModeID** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht mit der TTS-Moduseinstellung des kompilierten Zeichens übereinstimmt.

 

> [!Note]  
> Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück. Wenn das Laden der Sprach-Engine jedoch ungewöhnlich lange dauert, erhalten Sie möglicherweise einen Fehler, der angibt, dass für die Abfrage ein Time out aufgetreten ist.

 

## <a name="see-also"></a>Weitere Informationen

[**LanguageID-Eigenschaft**](languageid-property.md)


 

 




