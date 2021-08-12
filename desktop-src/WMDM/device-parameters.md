---
title: Geräteparameter
description: Geräteparameter
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Medien Geräte-Manager,Geräteparameter
- Geräte-Manager,Geräteparameter
- Programmierhandbuch, Geräteparameter
- Dienstanbieter,Geräteparameter
- Erstellen von Dienstanbietern,Geräteparameter
- Geräteparameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585349"
---
# <a name="device-parameters"></a>Geräteparameter

Windows Media Geräte-Manager verwendet Geräteparameter, um das Verhalten eines Geräts zu steuern. Diese Parameter werden der Registrierung wie in der Installationsdatei (INF-Datei) des Geräts angegeben hinzugefügt. In der folgenden Tabelle sind die Geräteparameter aufgeführt, Windows Media Geräte-Manager abfragen.



| Name des Geräteparameters | Registrierungsdatentyp | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ SZ**        | Ein Wert, der die CLSID des Dienstanbieters angibt, der dieses Gerät steuert. Dieser Parameter ist für die PnP-Unterstützung obligatorisch.<br/> Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein. Dieser Parameter ist erforderlich, um Plug & Play (PnP) unter Windows Media Geräte-Manager. Weitere Informationen finden Sie unter [Aktivieren von PnP für Geräte.](enabling-pnp-for-devices.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | Optionaler Wert, der die bevorzugte Übertragungsgröße angibt, die Windows Media Geräte-Manager Lese- und Schreibvorgängen verwendet. Wenn sie nicht angegeben wird, wird eine Standardübertragungsgröße verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | Optionaler Parameter, der angibt, Windows Media Geräte-Manager Inhalt nach Metadaten organisiert, während Geräteinhalte anwendungen präsentiert werden. Wenn dieser Wert fehlt, wird der Standardwert 0 verwendet.<br/> Wenn Anwendungen den Inhalt in den Speichern eines portablen Audioplayers aufzählen, kann Windows Media Geräte-Manager inhalte nach Metadaten organisiert präsentieren. Dies ist besonders nützlich für Geräte mit großer Speicherkapazität.<br/> Anwendungen und Geräte können dieses Verhalten steuern. Geräte geben ihre Präferenz über den Geräteparameter *UseMetadataViews an.*<br/> Die folgenden beiden ganzzahligen Werte werden unterstützt:<br/> Fordert an, dass Inhalte den Anwendungen genau so präsentiert werden, wie sie im Dateisystem des Geräts organisiert sind.<br/> Fordert an, dass der Inhalt den Anwendungen präsentiert wird, die nach Metadaten organisiert sind.<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | Optionaler Parameter, der angibt, ob das Gerät im Explorer Windows werden soll. Der Wert 1 gibt an, dass das Gerät im Explorer Windows werden soll. Weitere Informationen finden Sie unter [Requirements for Portable Audio Players to Appear in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | Optionaler Parameter, der Windows Media Geräte-Manager, dass der Dienstanbieter **IMDSPDevice3,** **IMDSPObject2** und **IMDSPStorage4 unterstützt.** Ohne dieses Flag wird Windows Media Geräte-Manager diese Schnittstellen nie aufrufen. Der Wert 1 gibt an, dass diese Schnittstellen unterstützt werden.<br/> Dieses Flag ist für Dienstanbieter erforderlich, die eine Synchronisierung mit Windows Media Player. (Siehe [Aktivieren der Synchronisierung mit Windows Media Player](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codieren der INF-Datei**

Der folgende Beispielcode aus der INF-Datei eines Geräts veranschaulicht das Festlegen einiger Geräteparameter während der Geräteinstallation.


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> <dt>

[**IMDServiceProvider2-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





