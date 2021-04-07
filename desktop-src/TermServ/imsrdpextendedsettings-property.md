---
title: IMsRdpExtendedSettings Property-Eigenschaft
description: Enthält eine benannte Eigenschaft.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Eigenschaften Eigenschaften Remotedesktopdienste
- Eigenschafts Eigenschaft Remotedesktopdienste, imsrdpextendedsettings-Schnittstelle
- Imsrdpextendedsettings-Schnittstelle Remotedesktopdienste, Property-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745352"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>Imsrdpextendedsettings::P roperty-Eigenschaft

Enthält eine benannte Eigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>Eigenschaftswert

Der benannte Eigenschafts Wert.

| Eigenschaftenname | Datentyp | Access | Kann geändert werden, nachdem die Verbindung gestartet wurde. | BESCHREIBUNG |
|----------|-----------|--------|-----------------------------------------|-------------|
| Connectdechildsession | **VT \_ bool** | Lesen/Schreiben | Ja | Das Festlegen dieser Eigenschaft auf **true** bewirkt, dass das Client Steuerelement eine Verbindung mit der untergeordneten Sitzung auf dem lokalen Computer anstelle eines Remote Servers herstellt. Wenn diese Eigenschaft auf **true** festgelegt ist, können Sie keine Verbindung mit einem Remote Server herstellen, da alle Verbindungen zu localhost umgeleitet werden. Weitere Informationen zu untergeordneten Sitzungen finden Sie unter untergeordnete [Sitzungen](child-sessions.md). |
| Disablekredentialsdelegation | **VT \_ bool** | Lesen/Schreiben | Nein | **True** gibt an, dass Anmelde Informationen nicht an den Remote Server gesendet werden. |
| Enableframebufferredirect | **VT \_ bool** | Lesen/Schreiben | Nein | **True** gibt an, dass eine Frame Puffer Umleitung versucht wird. Bei einer Loopback Verbindung (auf dem Client und auf dem Server) ermöglicht die Frame Puffer Umleitung, dass der Arbeitsspeicher für den Frame Puffer zwischen den Sitzungen gemeinsam verwendet wird. |
| Enablehardwaremode | **VT \_ bool**  | Nur schreiben | Nein | **True** gibt an, dass die Hardwareunterstützung mit der Grafik Decodierung versucht wird. |
| Ignorecursoren | **VT \_ bool** | Nur schreiben | Nein | **True** gibt an, dass vom Remote Server gesendete Cursor ignoriert werden. |
| Manualclipboardsyncenabled | **VT \_ bool** | Lesen/Schreiben | Ja | Wenn diese Eigenschaft auf " **true** " festgelegt wird, werden die lokalen und Remote-zwischen Ablagen nicht automatisch synchron gehalten. Stattdessen muss die [**imsrdpclipboard**](imsrdpclipboard.md) -Schnittstelle verwendet werden, um Zwischenablage Formate aus der lokalen Zwischenablage mit der Remote Zwischenablage und der Remote Zwischenablage in die lokale Zwischenablage zu synchronisieren. |
| ZoomLevel | **_VT \_ UI4_* | Lesen/Schreiben | Ja | Implementiert das Zoom Feature mithilfe des RDP-ActiveX-Steuer Elements. Die Zoom Funktion ist im Menü **System** von RDP verfügbar. Die **Zoomlevel** -Eigenschaft hat keine Auswirkung auf den RemoteApp-Modus und den Vollbildmodus. [**Imsrdpclientadvancedsettings:: smartsizing**](imsrdpclientadvancedsettings-smartsizing.md) und **Zoomlevel** schließen sich gegenseitig aus. |

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.<br/> |
| IID<br/>                      | IID \_ imsrdpextendedsettings ist definiert als 302d8188-0052-4807-806a-362b628fi9ac5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpextendedsettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





