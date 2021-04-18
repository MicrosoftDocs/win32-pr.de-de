---
title: Text Normalisierung für Text-zu-Sprache-Engines
description: Text Normalisierung für Text-zu-Sprache-Engines
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337987"
---
# <a name="text-to-speech-engines-text-normalization"></a>Text Normalisierung für Text-zu-Sprache-Engines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Bei der Normalisierung werden Zahlen, Abkürzungen, Akronyme und idiomatiken identifiziert und nach Bedarf in voll Text transformiert. Dies ist in der Regel auf dem Kontext des Satzes begründet.

Beispielsweise wird mit dem L&H truvoice American-TTS-Modul der Satz:

King George VI von England ist am 6. Februar 1952.

wird im **normalen Kontext** wie folgt gelesen:

   König George V I von England, starb am 6. Februar 19 52.

Unter dem **e-Mail-Kontext** wird Sie jedoch wie folgt gelesen:

   King George das sechste von England, verstarb am sechsten Februar 19 52.

Informationen zur Verwendung des kontexttags für den **Kontext** finden Sie in der Dokumentation zur agentprogrammierung [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).

 

 




