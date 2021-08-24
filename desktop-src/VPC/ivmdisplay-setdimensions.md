---
title: IVMDisplay SetDimensions-Methode (VPCCOMInterfaces.h)
description: Legt die Höhe und Breite der VM-Anzeige in Pixel fest.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- SetDimensions-Methode Virtueller PC
- SetDimensions-Methode Virtual PC , IVMDisplay-Schnittstelle
- IVMDisplay-Schnittstelle Virtueller PC, SetDimensions-Methode
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
ms.openlocfilehash: 5bbf1db342342e9fbb8c0eff2df18f9c2a76443a4d20014bad34934ccecd3dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473360"
---
# <a name="ivmdisplaysetdimensions-method"></a>IVMDisplay::SetDimensions-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*displayPixelWidth* \[ In\]
</dt> <dd>

Die Breite in Pixel. Der Wert muss zwischen den Werten 640 und 2048 sein. Wenn der Wert nicht gleichmäßig durch 8 teilbar ist, wird er auf das nächstuntere Vielfache von 8 reduziert.

</dd> <dt>

*displayPixelHeight* \[ In\]
</dt> <dd>

Die Höhe in Pixel. Der Wert muss zwischen den Werten 480 und 1920 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                         | Der *displayPixelWidth-Parameter* ist nicht gleichmäßig durch 8 teilbar, oder der *displayPixelWidth-* oder *displayPixelHeight-Parameter* liegt außerhalb der zulässigen Mindestwerte (640 x 480) oder maximal 2048 x 1920.<br/> |
| <dl> <dt>**VM \_ E \_ \_ TIMED OUT**</dt> <dt>0xA0040202</dt> </dl>                     | Die Auflösungsänderung wurde nicht rechtzeitig abgeschlossen.<br/>                                                                                                                                              |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                                                                                                                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                    | Der virtuelle Computer ist ungültig oder wird derzeit nicht ausgeführt.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ NO \_ DISPLAY**</dt> <dt>0xA0040850</dt> </dl>                    | Es konnte keine gültige Anzeige für den virtuellen Computer gefunden werden.<br/>                                                                                                                                                          |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | Die Im Gastbetriebssystem installierte Version der Integrationskomponenten unterstützt diesen Vorgang nicht.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Die Mindestgröße der Anzeige des virtuellen Computers beträgt 640 x 480 Pixel. Die maximale Größe beträgt 2048 x 1920. Versuche, die Anzeigegröße auf Werte außerhalb dieser Grenzwerte oder auf eine breite festzulegen, die nicht gleichmäßig durch 8 geteilt werden kann, führen dazu, dass ein **E \_ INVALIDARG-Fehler** zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

