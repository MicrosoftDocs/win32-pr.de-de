---
title: Ivmharddisk Convert-Methode (vpccominterfaces. h)
description: Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Konvertieren von Virtual PC-Methoden
- Convert-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Methode konvertieren
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478804"
---
# <a name="ivmharddiskconvert-method"></a>Ivmharddisk:: Convert-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.

## <a name="syntax"></a>Syntax


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*converteddiskimagepath* \[ in\]
</dt> <dd>

Der Pfad zur Ziel-Datenträger Image Datei.

</dd> <dt>

*converteddiskimagetype* \[ in\]
</dt> <dd>

Der Typ des Ziel Datenträger Images. Eine Liste der Werte finden Sie unter [**vmharddisktype**](vmharddisktype.md).

</dd> <dt>

*converttask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das zum Nachverfolgen des Abschlusses des Konvertierungsprozesses verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                        |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                   | Der *converteddiskimagepath* -Parameter ist leer, oder die VHD-Erweiterung für den Dateinamen fehlt.<br/>                                      |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                      | Ein Parameter ist **null**.<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl>   | Das System kann den vom *converteddiskimagepath* -Parameter angegebenen Pfad nicht finden.<br/>                                                 |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>      | Der *converteddiskimagepath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>      | Der *converteddiskimagepath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl>   | Der vom *converteddiskimagepath* -Parameter angegebene Pfad ist zu lang. Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt> </dl> | Entweder wird die virtuelle Festplatte verwendet, auf die von diesem Objekt verwiesen wird, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.<br/>                  |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>         | Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um diese virtuelle Festplatte zu konvertieren.<br/>                                                        |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>    | Die Datei, auf die vom *converteddiskimagepath* -Parameter verwiesen wird, ist bereits vorhanden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt> </dl>                   | Der *converteddiskimagepath* -Parameter muss entweder " **vmdisktype \_ Dynamic** " oder " **vmdisktype \_ FixedSize**" lauten.<br/>                          |
| <dl> <dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt> </dl>                        | Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, scheint kein gültiges Image zu sein.<br/>          |
| <dl> <dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die von diesem Objekt verwiesen wird, ist nicht vorhanden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                      | Das Image der virtuellen Festplatte kann nicht konvertiert werden, da die Anwendung heruntergefahren wird.<br/>                                            |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die Quelldatei bleibt nach dem Konvertierungs Vorgang intakt.

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

 

