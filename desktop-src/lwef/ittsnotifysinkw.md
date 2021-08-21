---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86cedf8c4a349da800f34f2f6acd7266f9cd0c3c383be9accb72dd162df8e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748708"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Die Engine muss über [**AudioStop,**](https://www.bing.com/search?q=**AudioStop**) [**AudioStart und**](https://www.bing.com/search?q=**AudioStart**) [**Visual aufrufen.**](https://www.bing.com/search?q=**Visual**) Der **visuelle** Rückruf muss IPA-Phoneme bereitstellen. (Das internationale phonetische Alphabet \[ IPA \] ist eine universelle Notation zum Beschreiben des phonetischen Inhalts der gesprochenen Kommunikation. Alle sprichtbaren Phoneme verfügen über Darstellungen in IPA. Details zu IPA finden Sie im Microsoft Speech \[ API-Spezifikationsteil des Speech SDK 4.0-Downloads unter \] [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)

Obwohl die [**visual-Benachrichtigung**](https://www.bing.com/search?q=**Visual**) recht gut ist, verwendet Microsoft Agent nur den **cIPAPhoneme-Wert,** um den Sprechschädchen zu animieren. Jede Mit Microsoft Agent kompatible Engine muss  einen eng synchronisierten Stream visueller Benachrichtigungen bereitstellen, der den phonetischen Inhalt der erzeugten Äußerung wiederspiegelt. In diesem Fall ist eine "relativ rechtzeitige Benachrichtigung" nicht ausreichend, da Sprecher-Hörer relativ empfindlich auf Abweichungen zwischen Deren Position und akustischem Inhalt reagieren. **Visuelle** Benachrichtigungen müssen sofort zurückgegeben werden.

 

 




