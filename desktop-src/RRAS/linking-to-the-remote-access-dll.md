---
title: Verknüpfen mit der Remote Zugriffs-dll
description: Wenn eine Anwendung statisch mit der rasapi32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der Remote Zugriffs Dienst nicht installiert ist.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858384"
---
# <a name="linking-to-the-remote-access-dll"></a>Verknüpfen mit der Remote Zugriffs-dll

Wenn eine Anwendung statisch mit der rasapi32-DLL verknüpft ist, kann die Anwendung nicht geladen werden, wenn der Remote Zugriffs Dienst nicht installiert ist. Eine RAS-Anwendung kann geladen werden, wenn RAS nicht mithilfe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) zum Laden der dll und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zum Abrufen von Zeigern auf die RAS-Funktionen installiert wird.

Die RAS-Funktionen befinden sich in RASAPI32.DLL. Die Import Bibliothek für diese Funktionen ist rasapi32. LIB. Um die RAS-Funktionen verwenden zu können, müssen die Programme die folgenden Dateien enthalten:



| Datei       | BESCHREIBUNG                                                                 |
|------------|-----------------------------------------------------------------------------|
| Shof. Micha      | Enthält die Prototypen, Konstanten und Strukturdefinitionen der RAS-Funktion. |
| Raserror. Micha | Enthält die RAS-Fehlercodes.                                               |



 

 

 