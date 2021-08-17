---
description: Windows Portable Geräte unterstützen die folgenden Ressourcenattribute.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Ressourcenattribute (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 303f43f1061dd9d8b05855b3c2af94a1ace3c071c12b308303b1524b255a6133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963513"
---
# <a name="resource-attributes"></a>Ressourcenattribute

Windows Portable Geräte unterstützen die folgenden Ressourcenattribute. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| attribute                                                  | VarType      | Beschreibung                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELÖSCHT \_ WERDEN**                  | **VT \_ BOOL** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Löschen der Ressource verfügt. Wenn sie nicht vorhanden ist, wird davon ausgegangen, dass sie false ist.                |
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN GELESEN \_ WERDEN**                    | **VT \_ BOOL** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für Lesezugriff verfügt. Wenn sie nicht vorhanden ist, wird davon ausgegangen, dass sie False ist.  |
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ KANN \_ SCHREIBEN**                   | **VT \_ BOOL** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für Schreibzugriff verfügt. Wenn sie nicht vorhanden ist, wird davon ausgegangen, dass sie false ist. |
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ OPTIMALE \_ \_ \_ LESEPUFFERGRÖßE**  | **VT \_ UI4**  | Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Lesedaten aus der Ressource verwenden soll.                                                  |
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ OPTIMALE \_ \_ \_ SCHREIBPUFFERGRÖßE** | **VT \_ UI4**  | Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Schreibvorgänge für die Ressource verwenden soll.                                                   |
| **\_GESAMTGRÖßE DES WPD-RESSOURCENATTRIBUTS \_ \_ \_**                  | **VT \_ UI8**  | Die Gesamtgröße der Ressourcendaten in Bytes.                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Eigenschaften**](properties-and-attributes.md)
</dt> </dl>

 

 




