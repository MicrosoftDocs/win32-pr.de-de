---
description: Die IDownloadJob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: IDownloadJob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cdd4f95a14df215017f9fd628497d15c6c7410e4a82cbfb53c076b2112899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049337"
---
# <a name="idownloadjob-properties"></a>IDownloadJob-Eigenschaften

Die [**IDownloadJob-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) definiert die folgenden Eigenschaften.



| Eigenschaft                                        | Beschreibung                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Ruft das aufruferspezifische Zustandsobjekt ab, das an die [**IUpdateDownloader.BeginDownload-Methode übergeben**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) wird.           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Ruft die Einstellung ab, die angibt, ob der Aufruf von [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) vollständig verarbeitet wurde. |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der Updates enthält, die in einem Download angegeben sind.                                                  |



 

 

 



