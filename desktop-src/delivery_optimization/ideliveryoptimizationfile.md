---
title: Ideliveryoptimizationfile-Schnittstelle
description: Implementieren Sie die ideliveryoptimizationfile-Schnittstelle, um den Status einer bestimmten Datei zu identifizieren.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Ideliveryoptimizationfile-Schnittstelle
- Ideliveryoptimizationfile-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341790"
---
# <a name="ideliveryoptimizationfile-interface"></a>Ideliveryoptimizationfile-Schnittstelle

Implementieren Sie die **ideliveryoptimizationfile** -Schnittstelle, um den Status einer bestimmten Datei zu identifizieren.

## <a name="members"></a>Member

Die **ideliveryoptimizationfile** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ideliveryoptimizationfile** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ideliveryoptimizationfile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.<br/> |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)      | Windows 10, Version 1709, \[ nur Desktop-Apps\]                                   |
| Unterstützte Mindestversion (Server)      | Windows Server, Version 1709, \[ nur Desktop-Apps\]                               |
| Header                        | Deliveryoptimization. h                                                           |
| IDL                           | Deliveryoptimization. idl                                                         |
| Bibliothek                       | Dosvc. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert. |
