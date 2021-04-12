---
title: Ttsmodeid (Eigenschaft)
description: Ttsmodeid (Eigenschaft)
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207222"
---
# <a name="ttsmodeid-property"></a>Ttsmodeid (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den für das Zeichen verwendeten TTS-Engine-Modus zurück oder legt ihn fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Ttsmodeid* *  \[  =  *modeid*\]



| Teil     | BESCHREIBUNG                                                             |
|----------|-------------------------------------------------------------------------|
| *Modeid* | Ein Zeichen folgen Ausdruck, der der Mode-ID einer Sprach-Engine entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft bestimmt die ID des TTS (Text-zu-Sprache-Engine) für die gesprochene Ausgabe eines Zeichens. Die Mode-ID für eine TTS-Engine ist eine formatierte Zeichenfolge, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert. Weitere Informationen finden Sie unter [zugreifen auf eine Sprach-Engine in Ihrem Code](accessing-a-speech-engine-in-your-code.md).

Das Festlegen dieser Eigenschaft überschreibt den Versuch des Servers, eine Engine basierend auf der kompilierten TTS-Einstellung des Zeichens und der aktuellen [**LanguageID**](languageid-property.md) -Einstellung des Zeichens zu laden. Wenn Sie jedoch eine Modus-ID für eine Engine angeben, die nicht installiert ist, oder wenn der Benutzer die Sprachausgabe im Microsoft-agenteigenschaftenblatt (**Audiooutput. aktiviert = false**) deaktiviert hat, löst der Server einen Fehler aus.

Wenn Sie nicht (oder nicht erfolgreich) eine TTS-Modus-ID für das Zeichen festgelegt haben, prüft der Server, ob die kompilierte TTS-Moduseinstellung des Zeichens mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens übereinstimmt und ob die zugehörige TTS-Engine installiert ist. Wenn dies der Fall ist, wird der "TTS"-Modus, der vom Zeichen für die gesprochene Ausgabe verwendet wird, und diese Eigenschaft gibt die Wenn dies nicht der Grund ist, fordert der Server eine kompatible SAPI-Sprach-Engine an, die der **LanguageID** des Zeichens entspricht, sowie das Geschlecht und das Alter, die für die ID des kompilierten Modus des Zeichens festgelegt sind. Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, ist die **LanguageID** die aktuelle Benutzersprache. Wenn keine übereinstimmende Engine gefunden werden kann, gibt die Abfrage für diese Eigenschaft eine leere Zeichenfolge für die Modus-ID der Engine zurück. Wenn Sie diese Eigenschaft Abfragen, wenn der Benutzer die Sprachausgabe im Microsoft-Agent-Eigenschaften Blatt (**Audiooutput. aktivierte = false**) deaktiviert hat, ist der Wert eine leere Zeichenfolge.

Durch Abfragen oder Festlegen dieser Eigenschaft wird die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde). Wenn jedoch die Engine, die in der kompilierten TTS-Einstellung des Zeichens angegeben ist, installiert ist und mit der Sprach-ID-Einstellung des Zeichens übereinstimmt, wird die Engine geladen, wenn das Zeichen geladen wird.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

> [!Note]  
> Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf dem System keine kompatible Soundunterstützung installiert ist.

 

> [!Note]  
> Das Festlegen der **ttsmodeid** kann fehlschlagen, wenn Speech.dll nicht installiert ist und die angegebene Engine nicht mit der kompilierten TTS-Moduseinstellung des Zeichens identisch ist.

 

> [!Note]  
> Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück. Wenn die Sprach-Engine jedoch eine ungewöhnlich lange Ladezeit benötigt, erhalten Sie möglicherweise eine Fehlermeldung, die angibt, dass die Abfrage abgelaufen ist.

 

## <a name="see-also"></a>Weitere Informationen

[**LanguageID (Eigenschaft)**](languageid-property.md)


 

 




