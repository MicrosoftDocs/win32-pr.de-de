---
description: Die iinstallationjob-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Iinstallationjob-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752096"
---
# <a name="iinstallationjob-properties"></a>Iinstallationjob-Eigenschaften

Die [**iinstallationjob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                            | BESCHREIBUNG                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Ruft das aufruferspezifische Zustands Objekt ab, das an die [**iupdateinstaller. begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) -Methode oder die [**iupdateinstaller. beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) -Methode übergeben wird.               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Ruft einen Wert ab, der angibt, ob ein Aufrufen der [**iupdateinstaller. begininstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) -Methode oder der [**iupdateinstaller. beginuninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) -Methode vollständig verarbeitet wird. |
| [**Updates**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Ruft eine Schnittstelle ab, die eine schreibgeschützte Auflistung der bei der Installation oder der Installation angegebenen Updates enthält.                                                                                                        |



 

 

 



