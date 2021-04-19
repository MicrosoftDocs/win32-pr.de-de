---
title: Ivmdisplay setdimensions-Methode (vpccominterfaces. h)
description: Legt die Höhe und Breite der VM-Anzeige in Pixel fest.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Setdimensions-Methode Virtual PC
- Setdimensions-Methode Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, setdimensions-Methode
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343055"
---
# <a name="ivmdisplaysetdimensions-method"></a>Ivmdisplay:: setdimensions-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Legt die Höhe und Breite der Anzeige des virtuellen Computers (VM) in Pixel fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Display Pixel Width* \[ in\]
</dt> <dd>

Die Breite in Pixel. Der Wert muss zwischen den Werten 640 und 2048 liegen. Wenn der Wert nicht gleichmäßig von 8 teilbar ist, wird er auf das nächst niedrigere Vielfache von 8 reduziert.

</dd> <dt>

*Display Pixel Height* \[ in\]
</dt> <dd>

Die Höhe in Pixel. Der Wert muss zwischen den Werten 480 und 1920 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                         | Der *displaypixelwidth* -Parameter ist von 8 nicht gleichmäßig teilbar, oder der *displaypixelwidth* -oder der *displaypixelheight* -Parameter liegt außerhalb des zulässigen Werts (640 x 480) oder Maximum 2048x1920).<br/> |
| <dl> <dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt> </dl>                     | Die Auflösungs Änderung wurde nicht rechtzeitig abgeschlossen.<br/>                                                                                                                                              |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                                                                                                                                               |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                    | Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ keine \_ Anzeige**</dt> <dt>0xa0040850</dt> </dl>                    | Es konnte keine gültige Anzeige für die VM gefunden werden.<br/>                                                                                                                                                          |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl> | Dieser Vorgang wird von der Version der Integrations Komponenten, die im Gast Betriebssystem installiert sind, nicht unterstützt.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Die minimale Größe der Anzeige des virtuellen Computers beträgt 640 x 480 Pixel. Die maximale Größe beträgt 2048 x 1920. Versucht, die Anzeige Größe auf Werte außerhalb dieser Grenzwerte oder auf eine beliebige Breite festzulegen, die nicht gleichmäßig von 8 teilbar ist, führt dazu, dass ein **E \_ invalidArg** -Fehler zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdisplay**](ivmdisplay.md)
</dt> </dl>

 

