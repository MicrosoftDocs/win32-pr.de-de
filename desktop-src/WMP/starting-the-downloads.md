---
title: Starten der Downloads
description: Starten der Downloads
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player,Download-Manager
- Onlineshops,Download-Manager
- Typ 2 Onlineshops,Download-Manager
- Windows Media Player,Starten von Downloads
- Onlineshops,Starten von Downloads
- Typ 2 Onlineshops,Starten von Downloads
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Starten von Downloads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995070"
---
# <a name="starting-the-downloads"></a>Starten der Downloads

Der Download beginnt, wenn der Benutzer auf **Herunterladen klickt.** Diese Schaltfläche heißt btnDownload im Code, und die Ereignishandlerfunktion für das **onClick-Ereignis** heißt "OnDownload".

"OnDownload" erstellt zunächst ein neues leeres **DownloadCollection-Objekt** und weist es einer lokalen Variablen zu.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Als Nächstes startet die Funktion jedes der fünf Elemente, die heruntergeladen werden, und speichert das **zurückgegebene DownloadItem-Objekt** in einem Array.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Der Code aktualisiert dann die Benutzeroberflächenelemente mit den Informationen zur Downloadsammlung und ihren Downloadelementen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




