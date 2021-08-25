---
title: SRModeID-Eigenschaft
description: SRModeID-Eigenschaft
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2ea6664230f9b2446cbe10a31a0129abb8bc52f0679bb6fdec0a1f0a8be211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960860"
---
# <a name="srmodeid-property"></a>SRModeID-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die spracherkennungs-Engine zurück, die das Zeichen verwendet, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Characters("**_CharacterID_*_"). SRModeID_ *  \[  =  *ModeID*\]



| Teil     | BESCHREIBUNG                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Ein Zeichenfolgenausdruck, der der Modus-ID einer Sprach-Engine entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die -Eigenschaft bestimmt die Spracherkennungs-Engine, die vom Zeichen für die Spracheingabe verwendet wird. Die Modus-ID für eine Spracherkennungs-Engine ist eine vom Sprachanbieter definierte formatierte Zeichenfolge, die die Engine eindeutig identifiziert. Weitere Informationen finden Sie unter [Zugreifen auf eine Sprach-Engine in Ihrem Code.](accessing-a-speech-engine-in-your-code.md)

Wenn Sie eine Modus-ID für eine nicht installierte Sprach-Engine angeben, der Benutzer die Spracherkennung deaktiviert hat (auf dem Microsoft Agent-Eigenschaftenblatt) oder wenn die Sprache der angegebenen Sprach-Engine nicht mit der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens übereinstimmen soll, löst der Server einen Fehler aus.

Wenn Sie diese Eigenschaft abfragen und die Spracherkennungs-Engine noch nicht (erfolgreich) festgelegt haben, gibt der Server die Modus-ID der Engine zurück, die SAPI basierend auf der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens zurückgibt. Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, gibt der -Agent die Modus-ID der Engine zurück, die SAPI basierend auf der Standardeinstellung für die Sprach-ID des Benutzers zurückgibt. Wenn keine übereinstimmende Engine verfügbar ist, gibt der Server eine leere Zeichenfolge ("") zurück. Das Abfragen dieser Eigenschaft erfordert nicht, dass [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) auf True festgelegt **ist.** Wenn Sie die -Eigenschaft jedoch abfragen, wenn die Spracheingabe deaktiviert ist, gibt der Server eine leere Zeichenfolge zurück.

Wenn die Spracheingabe aktiviert ist (im Fenster Erweiterte Zeichenoptionen), wird beim Abfragen oder Festlegen dieser Eigenschaft die zugeordnete Engine geladen (sofern sie noch nicht geladen ist) und die Spracherkennungsdienste gestartet. Das heißt, die Abhörtaste ist verfügbar, und der Tipp zum Lauschen wird angezeigt. (Die Abhörtaste und der Lauschende Tipp sind nur aktiviert, wenn sie auch unter Erweiterte Zeichenoptionen aktiviert sind.) Wenn Sie jedoch die -Eigenschaft abfragen, wenn Sprache deaktiviert ist, startet der Server keine Spracherkennungsdienste.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Die Anforderungen an die Sprach-Engine von Microsoft Agent basieren auf der Microsoft Speech-API. Engines, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können mit dem -Agent installiert und verwendet werden.

> [!Note]  
> Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf Ihrem System keine kompatible Soundunterstützung installiert ist.

 

> [!Note]  
> Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück. Wenn das Laden der Sprach-Engine jedoch ungewöhnlich lange dauert, erhalten Sie möglicherweise einen Fehler, der angibt, dass für die Abfrage ein Time out aufgetreten ist.

 

## <a name="see-also"></a>Weitere Informationen

[**LanguageID-Eigenschaft**](languageid-property.md)


 

 




