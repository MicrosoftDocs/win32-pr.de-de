---
title: LanguageID (Eigenschaft)
description: LanguageID (Eigenschaft)
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311039"
---
# <a name="languageid-property"></a>LanguageID (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Sprachen-ID für das Zeichen zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. * * * Zeichen* *  **("***Merkmal-ID***"). LanguageID** \[  =  *LanguageID*\]



Teil

BESCHREIBUNG

LanguageID

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (langid) für ein Zeichen ist ein 16-Bit-Wert, der von Windows definiert wird und aus einer primär Sprachen-ID und einer sekundären Sprach-ID besteht. Die folgenden Beispiele sind Werte für Sprachen, die vom Microsoft-Agent unterstützt werden. Informationen zum Bestimmen des Werts für andere Sprachen finden Sie in der *Platform SDK-Dokumentation*.

 

Arabisch

&H0401

Italienisch

&H0410

 

Baskisch

&H042D

Japanisch

&H0411

 

Chinesisch (vereinfacht)

&H0804

Koreanisch

&H0412

 

Chinesisch (traditionell)

&H0404

Norwegisch

&H0414

 

Kroatisch

&H041A

Polnisch

&H0415

 

Tschechisch

&H0405

Portugiesisch (Portugal)

&H0816

 

Dänisch

&H0406

Portugiesisch (Brasilien)

&H0416

 

Niederländisch

&H0413

Rumänisch

&H0418

 

Englisch (Großbritannien)

&H0809

Russisch

&H0419

 

Englisch (USA)

&H0409

Slowakisch

&H041B

 

Finnisch

&H040B

Slowenisch

&H0424

 

Französisch

&H040C

Spanisch

&H0C0A

 

Deutsch

&H0407

Schwedisch

&H041D

 

Griechisch

&H0408

Thailändisch

&H041E

 

Hebräisch

&H040D

Türkisch

&H041F

 

Ungarisch

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die **LanguageID** nicht für das Zeichen festlegen, wird die Sprach-ID der aktuellen Systemsprachen-ID angezeigt, wenn die entsprechende dll der Agent-Sprache installiert ist. andernfalls ist die Sprache des Zeichens Englisch (USA).

Diese Eigenschaft bestimmt auch die Sprache für Word-Sprechblasen Text, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt.

Wenn Sie versuchen, die **LanguageID** für ein Zeichen festzulegen, und die Agent-sprach-dll für diese Sprache nicht installiert ist oder eine Anzeige Schriftart für die Sprach-ID nicht verfügbar ist, löst der-Agent einen Fehler aus, und **LanguageID** bleibt bei der letzten Einstellung.

Wenn Sie diese Eigenschaft festlegen, wird kein Fehler ausgegeben, wenn keine übereinstimmenden Sprach-Engines für die Sprache vorhanden sind. Wenn Sie feststellen möchten, ob eine kompatible Sprach-Engine für **LanguageID** verfügbar ist, überprüfen Sie [**srmodeid**](srmodeid-property.md) oder [**ttsmodeid**](ttsmodeid-property.md). Wenn Sie **LanguageID** nicht festlegen, wird Sie auf die Einstellung Benutzer-ID der Standardsprache festgelegt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Wenn Sie **LanguageID** auf eine Sprache festlegen, die bidirektionalen Text (z. b. Arabisch oder Hebräisch) unterstützt, aber das System, auf dem Ihre Anwendung ausgeführt wird, nicht über eine bidirektionale Unterstützung verfügt, wird der Text in der Wort Sprechblase in logischer und nicht in Anzeige

 

## <a name="see-also"></a>Weitere Informationen

[**Srmodeid-Eigenschaft**](srmodeid-property.md), [ **ttsmodeid-Eigenschaft**](ttsmodeid-property.md)


 

 




