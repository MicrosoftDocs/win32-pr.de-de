---
title: Ittsnotifysinkw
description: Ittsnotifysinkw
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389944"
---
# <a name="ittsnotifysinkw"></a>Ittsnotifysinkw

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Engine muss über [**audiostop**](https://www.bing.com/search?q=**AudioStop**), [**audiostart**](https://www.bing.com/search?q=**AudioStart**)und [**Visual**](https://www.bing.com/search?q=**Visual**)aufgerufen werden. Der **visuelle** Rückruf muss IPA-Phonemes bereitstellen. (Das internationale phonetische Alphabet \[ IPA \] ist eine universelle Notation zum Beschreiben des phonetischen Inhalts der gesprochenen Kommunikation. Alle speakbaren Phoneme verfügen über Darstellungen in IPA. Details zur IPA-Datei finden Sie in der Microsoft Speech-API-Spezifikation \[ Teil des Sprach-SDK 4,0-Downloads \] unter [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)

Obwohl die [**visuelle**](https://www.bing.com/search?q=**Visual**) Benachrichtigung recht umfangreich ist, verwendet der Microsoft-Agent nur den **cipaphoneme** -Wert, um den Mund zu animieren, wenn das Zeichen spricht. Alle Microsoft-Agent-kompatiblen Module müssen einen eng synchronisierten Stream von **visuellen** Benachrichtigungen bereitstellen, die den phonetischen Inhalt der erzeugten Äußerung widerspiegeln. In diesem Fall ist die "relativ rechtzeitige Benachrichtigung" nicht ausreichend, da Sprecher der Sprech Anwendung recht sensibel auf Abweichungen zwischen mundposition und Akustik Inhalt sind. **Visuelle** Benachrichtigungen müssen umgehend zurückgegeben werden.

 

 




