---
title: Übergeordnete ivmharddisk-Eigenschaft (vpccominterfaces. h)
description: Übergeordnetes Element der differenzierenden virtuellen Festplatte.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Virtueller PC der übergeordneten Eigenschaft
- Übergeordnete Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Parent-Eigenschaft
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
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949385"
---
# <a name="ivmharddiskparent-property"></a>Ivmharddisk::P Arent-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Legt das [**ivmharddisk**](ivmharddisk.md) -Objekt fest, das dem übergeordneten Festplatten Abbild zugeordnet ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                                               | Dabei handelt es sich nicht um eine differenzierende Festplatte, daher hat Sie kein übergeordnetes Element.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt> </dl> | Das System konnte die übergeordnete virtuelle Festplatten Datei nicht finden.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt> </dl> | Das System konnte den Pfad zur übergeordneten virtuellen Festplatten Datei nicht finden.<br/>                                                                                                                                                                                                   |
| <dl> <dt>VM \_ E \_ HD- \_ Abbild \_ Öffnen \_ fehlschlagen</dt> <dt>0xa004067c</dt> </dl>                  | Fehler beim Öffnen der aktuellen Festplatten Abbild Datei.<br/>                                                                                                                                                                                               |
| <dl> <dt>VM \_ E \_ HD- \_ Abbild \_ Zugriff</dt> <dt>0xa0040681</dt> </dl>                      | Fehler beim Zugriff auf die aktuelle Festplatten Abbild Datei.<br/>                                                                                                                                                                                             |
| <dl> <dt>VM \_ E \_ - \_ \_ ID \_ </dt> des übergeordneten untergeordneten Elements <dt>0xa0040685</dt> </dl>            | Das virtuelle Festplatten Abbild, das vom übergeordneten Parameter gefunden wird, hat nicht die gleiche ID wie das unter *geordnete* Datenträger Image. Stellen Sie sicher, dass das übergeordnete virtuelle Festplatten Image, das vom über *geordneten* Parameter gefunden wird, dem Image entspricht, das zum Erstellen des differenzierenden virtuellen Festplatten Abbilds verwendet wurde.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur mit differenzierenden Festplatten Abbildern gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddisk**](ivmharddisk.md)
</dt> </dl>

 

