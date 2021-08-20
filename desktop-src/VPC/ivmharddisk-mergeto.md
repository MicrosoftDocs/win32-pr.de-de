---
title: IVMHardDisk MergeTo-Methode (VPCCOMInterfaces.h)
description: Führt eine differenzierende virtuelle Festplatte mit allen ihren über- und zugehörigen Datenträgern zusammen.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- MergeTo-Methode Virtueller PC
- MergeTo-Methode Virtual PC , IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, MergeTo-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f54c3e7cfcd328adcea355e90ff60d92590fb694915a3e682a6240b656e655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123717"
---
# <a name="ivmharddiskmergeto-method"></a>IVMHardDisk::MergeTo-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Datenträgern (bis einschließlich der übergeordneten Stammfestplatte) mit einer neuen Festplattendatei zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newDiskImagePath* \[ In\]
</dt> <dd>

Der Pfad zum neuen Zieldatenträgerimage, in dem die ausgewählten Datenträgerimages zusammengeführt werden.

</dd> <dt>

*newDiskImageType* \[ In\]
</dt> <dd>

Der Typ des neuen Zieldatenträgerimages. Die für das neue Zieldatenträgerimage zulässigen Imagetypen sind **vmDiskType \_ Dynamic** und **vmDiskType \_ FixedSize.** Weitere Informationen finden Sie unter [**VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) mit dem der Abschluss des Zusammenführungsprozesses nachverfolgt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                      | Ein Parameter ist **NULL.**<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                   | Der *newDiskImagePath-Parameter* ist leer.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl>   | Das System kann die durch den *newDiskImagePath-Parameter* angegebene Datei nicht finden.<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)**</dt> <dt>0X80070003</dt> </dl>   | Das System kann den vom *newDiskImagePath-Parameter* angegebenen Pfad nicht finden.<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Der *newDiskImagePath-Parameter* enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ?<>/ \| ":").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Der *newDiskImagePath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Der vom *newDiskImagePath-Parameter* angegebene Pfad ist zu lang. Der Pfad muss weniger als 260 Zeichen lang sein.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Entweder wird die virtuelle Festplatte verwendet, auf die dieses Objekt verweist, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.<br/>                                                                                                                                                                                |
| <dl> <dt>**VM \_ E \_ WRONG HD IMAGE \_ \_ \_ TYPE**</dt> <dt>0xA004067B</dt> </dl>                   | Dieser Fehler wird entweder verursacht, weil das image der virtuellen Festplatte, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, kein differenzierendes Datenträgerimage ist oder weil der Parameter *newDiskImageType* keiner der akzeptierten Werte ist, **vmDiskType \_ Dynamic** oder **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ALREADY \_ EXISTS)**</dt> <dt>0x800700b7</dt> </dl>    | Die Datei, auf die der *newDiskImagePath-Parameter* verweist, ist bereits vorhanden.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Das Hostvolume verfügt nicht über genügend Speicherplatz, um diese virtuelle Festplatte zusammenzuführen.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**VM \_ \_E \_ ÜBERGEORDNETER PFAD \_ NICHT \_ GEFUNDEN**</dt> <dt>0XA0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die dieses Objekt verweist, ist nicht vorhanden.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**VM \_ HERUNTERFAHREN \_ \_ DER \_ E-APP**</dt> <dt>0xA0040209</dt> </dl>                      | Das Image der virtuellen Festplatte kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

