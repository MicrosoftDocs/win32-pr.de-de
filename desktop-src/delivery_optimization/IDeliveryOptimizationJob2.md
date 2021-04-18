---
title: IDeliveryOptimizationJob2-Schnittstelle
description: 'Weitere Informationen finden Sie hier: IDeliveryOptimizationJob2-Schnittstelle'
keywords:
- IDeliveryOptimizationJob2-Schnittstelle
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344835"
---
# <a name="ideliveryoptimizationjob2-interface"></a>IDeliveryOptimizationJob2-Schnittstelle

Der IDeliveryOptimizationJob2 ermöglicht das Hinzufügen einer einzelnen Datei zum Download Auftrag und das sofortige Abrufen der Datei. Diese Schnittstelle unterstützt auch das Festlegen und das erhalten Optionaler Auftrags Eigenschaften.

## <a name="members"></a>Member

Die **IDeliveryOptimizationJob2** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IDeliveryOptimizationJob2** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDeliveryOptimizationJob2** -Schnittstelle verfügt über diese Methoden.

| Methode                                              | BESCHREIBUNG                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Diese Methode wird nicht verwendet.                                       |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10, Version 1803, \[ nur Desktop-Apps\]                                   |
| Unterstützte Mindestversion (Server) | Windows Server, Version 1709, \[ nur Desktop-Apps\]                               |
| Header                   | Deliveryoptimization. h                                                           |
| IDL                      | Deliveryoptimization. idl                                                         |
| Bibliothek                  | Dosvc. lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert. |
