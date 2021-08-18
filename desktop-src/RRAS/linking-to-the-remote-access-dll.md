---
title: Verknüpfen mit der REMOTEZUGRIFFS-DLL
description: Wenn eine Anwendung statisch mit der RASAPI32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der RAS-Dienst nicht installiert ist.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b98757320cf9a166e741eb10ace8607d0287740a5494ca20fcc431b16b4367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790650"
---
# <a name="linking-to-the-remote-access-dll"></a>Verknüpfen mit der REMOTEZUGRIFFS-DLL

Wenn eine Anwendung statisch mit der RASAPI32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der RAS-Dienst nicht installiert ist. Eine RAS-Anwendung kann geladen werden, wenn RAS nicht installiert ist, indem [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) zum Laden der DLL und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zum Abrufen von Zeigern auf die RAS-Funktionen verwendet wird.

Die RAS-Funktionen befinden sich in RASAPI32.DLL. Die Importbibliothek für diese Funktionen ist RASAPI32. Lib. Um die RAS-Funktionen verwenden zu können, müssen Ihre Programme die folgenden Dateien enthalten:



| Datei       | Beschreibung                                                                 |
|------------|-----------------------------------------------------------------------------|
| RAS. H      | Enthält die RAS-Funktionsprototypen, Konstanten und Strukturdefinitionen. |
| RASERROR. H | Enthält die RAS-Fehlercodes.                                               |



 

 

 