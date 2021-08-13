---
title: IVMHardDisk Compact-Methode (VPCCOMInterfaces.h)
description: Komprimiert ein dynamisch erweiterbares virtuelles Festplattenimage.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact-Methode Virtueller PC
- Compact-Methode Virtual PC , IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, Compact-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2ae6c8bcb4237f98c8bcb47089294b202e3e9c45e51351c9818a08e2a295ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472165"
---
# <a name="ivmharddiskcompact-method"></a>IVMHardDisk::Compact-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Komprimiert ein dynamisch erweiterbares virtuelles Festplattenimage.

## <a name="syntax"></a>Syntax


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*compactTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) mit dem der Abschluss des Komprimierungsprozesses nachverfolgt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                    |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                      | Der Parameter ist **NULL.**<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Das virtuelle Festplattenimage, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, wird verwendet.<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Das Hostvolume verfügt nicht über genügend Speicherplatz, um eine temporäre Datei zu erstellen, die für die Komprimierung dieses virtuellen Festplattenimages benötigt wird.<br/>     |
| <dl> <dt>**VM \_ E \_ APP \_ SHUTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | Das Image der virtuellen Festplatte kann nicht komprimiert werden, da die Anwendung heruntergefahren wird.<br/>                                            |
| <dl> <dt>**VM \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | Das virtuelle Festplattenimage, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, ist als schreibgeschützt gekennzeichnet.<br/>                     |
| <dl> <dt>**VM \_ E \_ WRONG HD IMAGE \_ \_ \_ TYPE**</dt> <dt>0xA004067B</dt> </dl>                   | Das image der virtuellen Festplatte, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, muss ein **vmDiskTypeDynamic-Imagetyp** sein.<br/> |
| <dl> <dt>**VM \_ E \_ INVALID \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | Das image der virtuellen Festplatte, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, scheint kein gültiges Image zu sein.<br/>          |



 

## <a name="remarks"></a>Hinweise

Um ein dynamisch erweiterbares Festplattenimage zu komprimieren, sollte der freie Speicherplatz auf dem Datenträgerimage zunächst auf null festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

