---
title: IMsRdpExtendedSettings Property-Eigenschaft
description: Enthält eine benannte Eigenschaft.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Eigenschafteneigenschafts-Remotedesktopdienste
- Eigenschaftseigenschaft Remotedesktopdienste , IMsRdpExtendedSettings-Schnittstelle
- IMsRdpExtendedSettings-Schnittstelle Remotedesktopdienste , Eigenschaftseigenschaft
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
ms.openlocfilehash: 7deeb0e4d6d0f393bae09bacc9ff6709defe51bf6ca6128cbeb64e2f4f6e35cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138503"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings::P roperty-Eigenschaft

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

Der benannte Eigenschaftswert.

| Eigenschaftenname | Datentyp | Zugriff | Kann geändert werden, nachdem die Verbindung gestartet wurde. | Beschreibung |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **VT \_ BOOL** | Lesen/Schreiben | Ja | Das Festlegen dieser Eigenschaft **auf TRUE** führt dazu, dass das Clientsteuer steuerelement eine Verbindung mit der untergeordneten Sitzung auf dem lokalen Computer anstelle eines Remoteservers herstellen kann. Wenn diese Eigenschaft auf **TRUE festgelegt ist,** können Sie keine Verbindung mit einem Remoteserver herstellen, da alle Verbindungen an localhost umgeleitet werden. Weitere Informationen zu untergeordneten Sitzungen finden Sie unter [Untergeordnete Sitzungen.](child-sessions.md) |
| DisableCredentialsDelegation | **VT \_ BOOL** | Lesen/Schreiben | Nein | True **gibt an,** dass anmeldeinformationen nicht an den Remoteserver gesendet werden. |
| EnableFrameBufferRedirection | **VT \_ BOOL** | Lesen/Schreiben | Nein | True **gibt an,** dass versucht wird, die Framepufferumleitung umzuleiten. Bei einer Loopbackverbindung (derselbe Computer ist sowohl Client als auch Server) ermöglicht die Framepufferumleitung, dass der Arbeitsspeicher für den Framepuffer von den Sitzungen gemeinsam genutzt wird. |
| EnableHardwareMode | **VT \_ BOOL**  | Nur Schreiben | Nein | True **gibt an,** dass die Hardware beim Decodieren von Grafiken unterstützt wird. |
| IgnoreCursors | **VT \_ BOOL** | Nur Schreiben | Nein | True **gibt an,** dass vom Remoteserver gesendete Cursor ignoriert werden. |
| ManualClipboardSyncEnabled | **VT \_ BOOL** | Lesen/Schreiben | Ja | Das Festlegen dieser Eigenschaft **auf TRUE** bedeutet, dass die lokale und die Remoteablage nicht automatisch synchronisiert werden. Stattdessen muss [**die IMsRdpClipboard-Schnittstelle**](imsrdpclipboard.md) verwendet werden, um Zwischenablageformate aus der lokalen Zwischenablage mit der Remoteablage und der Remoteablage mit der lokalen Zwischenablage zu synchronisieren. |
| ZoomLevel | ***VT \_ UI4** | Lesen/Schreiben | Ja | Implementiert das Zoomfeature mithilfe des RDP-ActiveX Steuerelements. Das Zoomfeature ist im **Menü System** von RDP verfügbar. Die **ZoomLevel-Eigenschaft** hat keine Auswirkungen im RemoteApp-Modus und im Vollbildmodus. [**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) und **ZoomLevel** schließen sich gegenseitig aus. |

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf7-b1ef-4479-9674-1bd6ea465258 definiert.<br/> CLSID \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.<br/> CLSID \_ MsRdpClient9NotSafeForScripting ist als 8B918B82-7985-4C24-89DF-C33AD2BBFBCD definiert.<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings ist als 302D8188-0052-4807-806A-362B628F9AC5 definiert.<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





