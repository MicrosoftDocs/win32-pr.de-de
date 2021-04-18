---
title: Srmodeid (Eigenschaft)
description: Srmodeid (Eigenschaft)
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341684"
---
# <a name="srmodeid-property"></a>Srmodeid (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die sprach Erkennungs-Engine zurück, die das Zeichen verwendet.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Srmodeid* *  \[  =  *modeid*\]



| Teil     | BESCHREIBUNG                                                             |
|----------|-------------------------------------------------------------------------|
| *Modeid* | Ein Zeichen folgen Ausdruck, der der Mode-ID einer Sprach-Engine entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die-Eigenschaft bestimmt die sprach Erkennungs-Engine, die vom Zeichen für die Spracheingabe verwendet wird. Die Mode-ID für eine Spracherkennungs-Engine ist eine formatierte Zeichenfolge, die vom Sprachanbieter definiert wird, der die Engine eindeutig identifiziert. Weitere Informationen finden Sie unter [zugreifen auf eine Sprach-Engine in Ihrem Code](accessing-a-speech-engine-in-your-code.md).

Wenn Sie eine Modus-ID für eine Sprach-Engine angeben, die nicht installiert ist, wenn der Benutzer die Spracherkennung deaktiviert hat (auf dem Eigenschaften Blatt des Microsoft-Agents) oder wenn die Sprache der angegebenen Sprach-Engine nicht mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens identisch ist, löst der Server einen Fehler aus.

Wenn Sie diese Eigenschaft Abfragen und die Spracherkennungs-Engine nicht bereits (erfolgreich) festgelegt haben, gibt der Server die Mode-ID der Engine zurück, die SAPI basierend auf der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens zurückgibt. Wenn Sie die **LanguageID** des Zeichens nicht festgelegt haben, gibt der-Agent die Mode-ID der Engine zurück, die von SAPI basierend auf der Standardeinstellung für die Sprach-ID des Benutzers zurückgegeben wird. Wenn keine übereinstimmende Engine vorhanden ist, gibt der Server eine leere Zeichenfolge ("") zurück. Das Abfragen dieser Eigenschaft erfordert nicht, dass " [**speechinput. aktiviert**](https://www.bing.com/search?q=**SpeechInput.Enabled**) " auf " **true**" festgelegt ist. Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Spracheingabe deaktiviert ist, gibt der Server eine leere Zeichenfolge zurück.

Wenn die Spracheingabe aktiviert ist (im Fenster Erweiterte Zeichen Optionen), wird durch das Abfragen oder Festlegen dieser Eigenschaft die zugeordnete Engine geladen (falls Sie nicht bereits geladen wurde), und die Sprachdienste werden gestartet. Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden. (Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

> [!Note]  
> Diese Eigenschaft gibt auch die leere Zeichenfolge zurück, wenn auf dem System keine kompatible Soundunterstützung installiert ist.

 

> [!Note]  
> Das Abfragen dieser Eigenschaft gibt in der Regel keinen Fehler zurück. Wenn die Sprach-Engine jedoch eine ungewöhnlich lange Ladezeit benötigt, erhalten Sie möglicherweise eine Fehlermeldung, die angibt, dass die Abfrage abgelaufen ist.

 

## <a name="see-also"></a>Weitere Informationen

[**LanguageID (Eigenschaft)**](languageid-property.md)


 

 




