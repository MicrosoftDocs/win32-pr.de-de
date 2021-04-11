---
title: ADSI-Attribut Änderungs Typen (IADs. h)
description: Wird verwendet \_ \_ , um den Typ des Vorgangs anzugeben, der ausgeführt werden soll, wenn ein Attribut mit der IDirectoryObject setobjectattributes-Methode geändert wird.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- Typen von Attribut Änderungen ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040320"
---
# <a name="adsi-attribute-modification-types"></a>Typen von ADSI-Attribut Änderungen

Die folgenden Konstanten werden zusammen mit dem **dwcontrolcode** -Member der [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur verwendet, um den Typ des Vorgangs anzugeben, der ausgeführt werden soll, wenn ein Attribut mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode geändert wird. Weitere Informationen zum Verwenden dieser Werte finden Sie unter [Ändern von Attributen mit ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS ist \_ \_ klar**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Bewirkt, dass alle Attributwerte aus einem-Objekt entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS- \_ \_ Update**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Bewirkt, dass die angegebenen Attributwerte aktualisiert werden.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**Werbung \_ \_ Anfügen**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Bewirkt, dass die angegebenen Attributwerte an die vorhandenen Attributwerte angehängt werden.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS- \_ \_ Löschung**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Bewirkt, dass die angegebenen Attributwerte aus einem-Objekt entfernt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Konstanten sollen mit der [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur in der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode verwendet werden. Diese Konstanten sollten nicht mit Membern der Enumeration der [**ADS- \_ Eigenschaften \_ Operation \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) verwechselt werden, die mit der [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                    |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Anzeige \_ \_ Informationen**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Ändern von Attributen mit ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





