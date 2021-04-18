---
description: Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribute.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Ressourcen Attribute (portabledevice. h)
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365624"
---
# <a name="resource-attributes"></a>Ressourcen Attribute

Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribute. Diese Attribute werden von den folgenden Methoden zurückgegeben:

-   [**Iportabledeviceresources:: getresourceattribute**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Attribut                                                  | VarType      | BESCHREIBUNG                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.**                  | **VT \_ bool** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Löschen der Ressource verfügt. Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist.                |
| **WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen**                    | **VT \_ bool** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für den Lesezugriff verfügt. Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist.  |
| **WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben**                   | **VT \_ bool** | Ein boolescher Wert, der angibt, ob ein Client über die Berechtigung zum Öffnen der Ressource für den Schreibzugriff verfügt. Wenn Sie nicht vorhanden ist, wird angenommen, dass Sie false ist. |
| **WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe**  | **VT \_ UI4**  | Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Lesevorgänge aus der Ressource verwenden soll.                                                  |
| **Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_** | **VT \_ UI4**  | Die empfohlene Puffergröße, die ein Aufrufer für gepufferte Schreibvorgänge für die Ressource verwenden soll.                                                   |
| **Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_**                  | **VT \_ UI8**  | Die Gesamtgröße der Ressourcen Daten in Bytes.                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften**](properties-and-attributes.md)
</dt> </dl>

 

 




