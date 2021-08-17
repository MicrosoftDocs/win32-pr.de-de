---
title: HTTP-Anforderungen für BITS-Downloads
description: BITS unterstützt HTTP- und HTTPS-Downloads und -Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9bd997bb5ef7f2125cfe7c3dc6850c0f44e81a8c3138f7f130952e31202a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010875"
---
# <a name="http-requirements-for-bits-downloads"></a>HTTP-Anforderungen für BITS-Downloads

BITS unterstützt HTTP- und HTTPS-Downloads und -Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt. Bei Downloads muss die **Head-Methode** des HTTP-Servers die Dateigröße zurückgeben, und die **Get-Methode** muss die Header Content-Range und Content-Length unterstützen. Daher überträgt BITS nur statische Dateiinhalte und generiert einen Fehler, wenn Sie versuchen, dynamischen Inhalt zu übertragen, es sei denn, das ASP-, ISAPI- oder CGI-Skript unterstützt die Header Content-Range und Content-Length.

BITS kann einen HTTP/1.0-Server verwenden, solange er die Anforderungen der **Methoden "Head"** und **"Get"** erfüllt.

Um das Herunterladen von Bereichen einer Datei zu unterstützen, muss der Server die folgenden Anforderungen unterstützen:

-   Zulassen, dass MIME-Header die standardmäßigen Content-Range- und Content-Type-Header sowie maximal 180 Bytes anderer Header enthalten.
-   Lassen Sie maximal zwei CR/LFs zwischen den HTTP-Headern und der ersten Begrenzungszeichenfolge zu.

 

 




