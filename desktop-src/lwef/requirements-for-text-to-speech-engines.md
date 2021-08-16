---
title: Anforderungen für Text-to-Speech-Engines
description: Anforderungen für Text-to-Speech-Engines
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746415"
---
# <a name="requirements-for-text-to-speech-engines"></a>Anforderungen für Text-to-Speech-Engines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Engine muss vollständig SAPI 4.0-kompatibel sein. Darüber hinaus muss die Engine auch die folgenden SAPI-Schnittstellen für markierte Text- und Lesezeichenbenachrichtigungen unterstützen. Diese Schnittstellen ermöglichen es dem Microsoft-Agent, die Ausgabe von Text in den Wortsprechblasen eines Zeichens zu beschleunigen und den Mund (oder eine Entsprechung) des Zeichens mit den gesprochenen Wörtern zu synchronisieren.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




