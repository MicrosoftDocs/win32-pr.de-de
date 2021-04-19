---
description: Die idownloadjob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Idownloadjob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345135"
---
# <a name="idownloadjob-properties"></a>Idownloadjob-Eigenschaften

Die [**idownloadjob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                        | BESCHREIBUNG                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Ruft das aufruferspezifische Zustands Objekt ab, das an die [**iupdatedownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) -Methode übergeben wird.           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Ruft die Einstellung ab, die angibt, ob der Aufrufen von [**iupdatedownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) vollständig verarbeitet wurde. |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der in einem Download angegebenen Updates enthält.                                                  |



 

 

 



