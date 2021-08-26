---
description: Die IInstallationJob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: IInstallationJob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb1604e69efc1d716b77be7303fc2148e93c0fe6d4fe2bc1ccd299f18ed9d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896980"
---
# <a name="iinstallationjob-properties"></a>IInstallationJob-Eigenschaften

Die [**IInstallationJob-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) definiert die folgenden Eigenschaften.



| Eigenschaft                                            | BESCHREIBUNG                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Ruft das aufruferspezifische Zustandsobjekt ab, das an die [**IUpdateInstaller.BeginInstall-**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) oder [**IUpdateInstaller.BeginUninstall-Methode übergeben**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) wird.               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Ruft einen Wert ab, der angibt, ob ein Aufruf der [**IUpdateInstaller.BeginInstall-**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) oder [**IUpdateInstaller.BeginUninstall-Methode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) vollständig verarbeitet wird. |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der Updates enthält, die in der Installation oder Deinstallation angegeben sind.                                                                                                        |



 

 

 



