---
title: IMsRdpClientNonScriptable5-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable4-Schnittstelle abgeleitet.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec338dbe07c4733bf80207298f23f388bf8f77c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479284"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>IMsRdpClientNonScriptable5-Schnittstelle

Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) -Schnittstelle abgeleitet. Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.

Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**imstscax**](imstscax-interface.md) -Objekt abgerufen, wobei **IID \_ IMsRdpClientNonScriptable5** übergeben wird.

## <a name="members"></a>Member

Die **IMsRdpClientNonScriptable5** -Schnittstelle erbt von [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientNonScriptable5** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                         | Zugriffstyp           | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Allowpromptingforanmeldeinformationen**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Benutzer zur Eingabe von Anmelde Informationen auffordert.<br/>                    |
| [**Disableconnectionbar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Lesegeschützt<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement die Verbindungs Leiste deaktivieren soll.<br/>                      |
| [**Disableremoteappcapscheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement den Server nicht auf RemoteApp-Funktionen überprüfen soll.<br/> |
| [**Getremotemonitorsboundingbox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Schreibgeschützt<br/>  | Gibt das Begrenzungs Rechteck des Remote Monitors an.<br/>                                                      |
| [**Remotemonitorcount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Schreibgeschützt<br/>  | Gibt die Anzahl der Remote Monitore an.<br/>                                                                     |
| [**Remotemonitorlayoutmatcheslocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Remote Monitor Layout mit dem Layout des lokalen Monitors identisch ist.<br/>                             |
| [**Usemultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lesen/Schreiben<br/> | Gibt an, ob das Remotedesktop ActiveX-Steuerelement mehrere Monitore verwenden soll.<br/>                           |
| [**Warnaboutdirectxredirect**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lesen/Schreiben<br/> | Diese Eigenschaft wird nicht verwendet.<br/>                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.<br/> CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.<br/> CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.<br/> CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 ist als 4f 6996d5-d7b1-412c-b0ff-063718566907 definiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

