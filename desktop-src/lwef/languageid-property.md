---
title: LanguageID-Eigenschaft
description: LanguageID-Eigenschaft
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13af9f7a508732444be83fd56cce2fad6c7d7a5c148e196e2c466db102d2e6e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748698"
---
# <a name="languageid-property"></a>LanguageID-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Sprach-ID für das Zeichen zurück oder legt sie fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.**Characters* *  **("**_CharacterID_*_"). LanguageID_* \[  =  *LanguageID*\]



Teil

BESCHREIBUNG

LanguageID

Eine lange ganze Zahl, die die Sprach-ID für das Zeichen angibt. Die Sprach-ID (LANGID) für ein Zeichen ist ein von Windows definierter 16-Bit-Wert, der aus einer primären Und einer sekundären Sprach-ID besteht. Die folgenden Beispiele sind Werte für Sprachen, die von Microsoft Agent unterstützt werden. Informationen zum Ermitteln des Werts für andere Sprachen finden Sie in der *Platform SDK-Dokumentation.*

 

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

## <a name="remarks"></a>Hinweise

Wenn Sie die **LanguageID** für das Zeichen nicht festlegen, ist ihre Sprach-ID die aktuelle Systemsprach-ID, wenn die entsprechende -Agent-Sprach-DLL installiert ist. Andernfalls ist die Sprache des Zeichens Englisch (USA).

Diese Eigenschaft bestimmt auch die Sprache für Den Wortsprechblasentext, die Befehle im Popupmenü des Zeichens und die Spracherkennungs-Engine. Außerdem wird die Standardsprache für die TTS-Ausgabe bestimmt.

Wenn Sie versuchen, die **LanguageID** für ein Zeichen zu setzen, und die DLL der -Agent-Sprache für diese Sprache nicht installiert ist oder keine Anzeigeschriftart für die Sprach-ID verfügbar ist, löst der -Agent einen Fehler aus, und **LanguageID** bleibt bei der letzten Einstellung.

Wenn Sie diese Eigenschaft festlegen, wird kein Fehler ausgegeben, wenn keine entsprechenden Sprach-Engines für die Sprache angezeigt werden. Überprüfen Sie [**SRModeID**](srmodeid-property.md) oder [**TTSModeID,**](ttsmodeid-property.md)um zu ermitteln, ob eine kompatible Sprach-Engine für **languageID** verfügbar ist. Wenn Sie **LanguageID nicht festlegen,** wird diese auf die Standardsprach-ID-Einstellung des Benutzers festgelegt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn Sie **LanguageID** auf eine Sprache festlegen, die bidirektionalen Text unterstützt (z. B. Arabisch oder Hebräisch), aber auf dem System, auf dem Ihre Anwendung ausgeführt wird, keine bidirektionale Unterstützung installiert ist, wird Text im Wortsprechblasen in logischer statt in anzeiger Reihenfolge angezeigt.

 

## <a name="see-also"></a>Weitere Informationen

[**SRModeID-Eigenschaft,**](srmodeid-property.md) [ **TTSModeID-Eigenschaft**](ttsmodeid-property.md)


 

 




