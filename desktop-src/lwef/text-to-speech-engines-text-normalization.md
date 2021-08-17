---
title: Textnormalisierung von Text-to-Speech-Engines
description: Textnormalisierung von Text-to-Speech-Engines
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd195212d52d9107aa8112c156bfd8dd6b33d00d2161bec624d182f0f12f78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347920"
---
# <a name="text-to-speech-engines-text-normalization"></a>Textnormalisierung von Text-to-Speech-Engines

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Normalisierung ist der Prozess, bei dem Zahlen, Abkürzungen, Akronyme und Idiomatiken identifiziert und bei Bedarf in Volltext transformiert werden, in der Regel basierend auf dem Kontext des Satzes.

Wenn Sie beispielsweise die L&H TruVoice American English TTS Engine verwenden, wird der folgende Satz verwendet:

KingIze VI. von Kürze ist am 6. Februar 1952 verendet.

wird im normalen **Kontext wie hier** gelesen:

   KingIze v. I. von Großbritannien, tod am 6. Februar, 1996, 1997

Unter dem **E-Mail-Kontext** wird es jedoch wie hier gelesen:

   Der sechste Von- und Sechste von Spanien, der am 6. Februar verstarb, ist 1997 1996 1996.

Informationen zur Verwendung des **Context Speech-Tags** finden Sie in der Dokumentation zur Agent-Programmierung [microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).

 

 




