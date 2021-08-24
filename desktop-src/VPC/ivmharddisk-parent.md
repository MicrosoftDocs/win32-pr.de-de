---
title: Übergeordnete IVMHardDisk-Eigenschaft (VPCCOMInterfaces.h)
description: Übergeordnetes Element der differenzierenden virtuellen Festplatte.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Übergeordnete Eigenschaft Virtueller PC
- Übergeordnete Eigenschaft Virtueller PC, IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, übergeordnete Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ba8d56ad09f7c8263e41b17d2e107a0a441408d22ffb604e95055c57fb21d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472100"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk::P arent-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das übergeordnete Element der differenzierenden virtuellen Festplatte ab und legt es fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt das [**IVMHardDisk-Objekt**](ivmharddisk.md) fest, das dem übergeordneten Festplattenimage zugeordnet ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                               | Dies ist keine differenzierende Festplatte, sodass sie kein übergeordnetes Element hat.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0x80070002</dt> </dl> | Das System konnte die übergeordnete virtuelle Festplattendatei nicht finden.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ VON \_ WIN32(FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN)</dt> <dt>0X80070003</dt> </dl> | Das System konnte den Pfad zur übergeordneten virtuellen Festplattendatei nicht finden.<br/>                                                                                                                                                                                                   |
| <dl> <dt>VM \_ E \_ HD IMAGE OPEN \_ \_ \_ FAIL</dt> <dt>0xA004067C</dt> </dl>                  | Fehler beim Öffnen der aktuellen Festplattenimagedatei.<br/>                                                                                                                                                                                               |
| <dl> <dt>VM \_ E \_ HD \_ IMAGE \_ ACCESS</dt> <dt>0xA0040681</dt> </dl>                      | Fehler beim Zugreifen auf die aktuelle Festplattenimagedatei.<br/>                                                                                                                                                                                             |
| <dl> <dt>VM \_ E \_ \_ ÜBERGEORDNETE UNTERGEORDNETE \_ \_ ID– NICHT ÜBEREINSTIMMENDE</dt> <dt>0xA0040685</dt> </dl>            | Das image der virtuellen Festplatte, das sich durch den *übergeordneten* Parameter befindet, weist nicht die gleiche ID wie das untergeordnete Datenträgerimage auf. Stellen Sie sicher, dass das image der übergeordneten virtuellen Festplatte, das sich im *übergeordneten* Parameter befindet, das gleiche Image ist, das zum Erstellen des differenzierenden virtuellen Festplattenimages verwendet wird.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur bei differenzierenden Festplattenimages gültig.

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

 

