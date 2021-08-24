---
title: IDeliveryOptimizationFile-Schnittstelle
description: Implementieren Sie die IDeliveryOptimizationFile-Schnittstelle, um den Status einer bestimmten Datei zu identifizieren.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- IDeliveryOptimizationFile-Schnittstelle
- IDeliveryOptimizationFile-Schnittstelle, beschrieben
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
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635740"
---
# <a name="ideliveryoptimizationfile-interface"></a>IDeliveryOptimizationFile-Schnittstelle

Implementieren Sie **die IDeliveryOptimizationFile-Schnittstelle,** um den Status einer bestimmten Datei zu identifizieren.

## <a name="members"></a>Member

Die **IDeliveryOptimizationFile-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDeliveryOptimizationFile-Schnittstelle** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**Getstats**](ideliveryoptimizationfile-getstats.md) | Gibt Download- und Uploadstatistiken für eine bestimmte Datei zurück.<br/> |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)      | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                                   |
| Unterstützte Mindestversion (Server)      | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]                               |
| Header                        | Deliveryoptimization.h                                                           |
| Idl                           | DeliveryOptimization.idl                                                         |
| Bibliothek                       | Dosvc.lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert. |
