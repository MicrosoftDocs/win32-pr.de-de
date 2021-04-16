---
title: HTTP-Anforderungen für Bits-Downloads
description: Bits unterstützt HTTP-und HTTPS-Downloads und-Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt.
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470965"
---
# <a name="http-requirements-for-bits-downloads"></a>HTTP-Anforderungen für Bits-Downloads

Bits unterstützt HTTP-und HTTPS-Downloads und-Uploads und erfordert, dass der Server das HTTP/1.1-Protokoll unterstützt. Für Downloads muss die **Head** -Methode des HTTP-Servers die Dateigröße zurückgeben, und die **Get** -Methode muss den Content-Range-Header und den Content-Length-Header unterstützen. Folglich überträgt Bits nur den Inhalt statischer Dateien und generiert einen Fehler, wenn Sie versuchen, dynamischen Inhalt zu übertragen, es sei denn, das ASP-, ISAPI-oder CGI-Skript unterstützt den Content-Range-Header und den Content-Length-Header.

Bits können einen HTTP/1.0-Server verwenden, sofern diese den Anforderungen an die **Head** -und **Get** -Methode erfüllen.

Der Server muss die folgenden Anforderungen erfüllen, um das Herunterladen von Bereichen einer Datei zu unterstützen:

-   Ermöglicht MIME-Headern das Einschließen der Standard Header für Content-Range und Content-Type sowie von maximal 180 bytes anderer Header.
-   Maximal zwei CR/LFS zwischen den HTTP-Headern und der ersten Begrenzungs Zeichenfolge zulassen.

 

 




