---
title: Fehlerprotokollierung in der HTTP-Server-API
description: Einige Arten von Fehlern werden von der HTTP-Server-API behandelt, anstatt zur Behandlung an eine Anwendung zurückgezahlt zu werden, da die Häufigkeit solcher Fehler andernfalls ein Ereignisprotokoll oder einen Anwendungshandler überfluten könnte.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- HTTP-Server-API, Fehlerprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c92c071929b61020b456d8ecabc81ebc0f05503c2f385b235afc323cf8dea33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130680"
---
# <a name="error-logging-in-the-http-server-api"></a>Fehlerprotokollierung in der HTTP-Server-API

Einige Arten von Fehlern werden von der HTTP-Server-API behandelt, anstatt zur Behandlung an eine Anwendung zurückgezahlt zu werden, da die Häufigkeit solcher Fehler andernfalls ein Ereignisprotokoll oder einen Anwendungshandler überfluten könnte.

In den folgenden drei Themen werden die verschiedenen Aspekte der HTTP Server-API-Fehlerprotokollierung beschrieben:

-   [Konfiguration](configuring-http-server-api-error-logging.md) Registrierungseinstellungen steuern, ob die HTTP-Server-API Fehler protokolliert, die maximal zulässige Größe von Protokolldateien und den Ort, an dem Protokolldateien gespeichert werden.
-   [Protokolldateiformat](format-of-the-http-server-api-error-logs.md) Die HTTP-Server-API erstellt Protokolldateien, die den W3C-Protokolldateikonventionen (World Wide Web Consortium) entsprechen, und kann mithilfe von Standardtools analysiert werden. Im Gegensatz zu W3C-Protokolldateien enthalten HTTP-Server-API-Protokolldateien jedoch keine Namen der Spalten.
-   [Protokollierte Fehlertypen](types-of-errors-logged-by-the-http-server-api.md) Die HTTP-Server-API protokolliert eine Vielzahl allgemeiner Fehler.

 

 




