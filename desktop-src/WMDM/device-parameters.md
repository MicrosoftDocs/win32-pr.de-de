---
title: Geräteparameter
description: Geräteparameter
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media Device Manager, Geräteparameter
- Device Manager, Geräteparameter
- Programmier Handbuch, Geräteparameter
- Dienstanbieter, Geräteparameter
- Erstellen von Dienstanbietern, Geräteparametern
- Geräteparameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309768"
---
# <a name="device-parameters"></a>Geräteparameter

Windows Media Device Manager verwendet Geräteparameter, um das Verhalten eines Geräts zu steuern. Diese Parameter werden der Registrierung entsprechend der Angabe in der Installationsdatei des Geräts (INF-Datei) hinzugefügt. In der folgenden Tabelle sind die Geräteparameter aufgeführt, die von Windows Media Device Manager werden.



| Geräteparameter Name | Registrierungs Datentyp | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Wmdmspclsid*         | **REG- \_ SZ**        | -Wert, der die CLSID des Dienstanbieters angibt, der dieses Gerät steuert. Dieser Parameter ist für die PNP-Unterstützung obligatorisch.<br/> Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein. Dieser Parameter ist für die Unterstützung von Plug & Play (PNP) unter Windows Media Device Manager obligatorisch. Weitere Informationen finden Sie unter [Aktivieren von PNP für Geräte](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *Optimaltransfersize* | **REG \_ DWORD**     | Optionaler Wert, der die bevorzugte Übertragungs Größe angibt, die von Windows Media Device Manager bei Lese-und Schreibvorgängen verwendet wird. Wenn Sie nicht angegeben wird, wird eine Standard Übertragungs Größe verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | Ein optionaler Parameter, der angibt, ob der Inhalt von Windows Media Device Manager bei der Darstellung von Geräte Inhalten an Anwendungen nach Metadaten organisiert wird. Wenn dieser Wert fehlt, wird der Standardwert 0 verwendet.<br/> Wenn Anwendungen den Inhalt der Speicher eines portablen Audioplayers aufzählen, können Windows Media-Device Manager den Inhalt nach Metadaten organisiert darstellen. Dies ist besonders bei Geräten mit umfangreicher Speicherkapazität nützlich.<br/> Anwendungen und Geräte können dieses Verhalten steuern. Geräte geben Ihre bevorzugte Einstellung durch den Geräteparameter *UseMetadataViews* an.<br/> Die folgenden beiden ganzzahligen Werte werden unterstützt:<br/> Fordert an, dass Inhalt den Anwendungen genau so angezeigt wird, wie er im Dateisystem des Geräts angeordnet ist.<br/> Fordert an, dass der Inhalt den von den Metadaten organisierten Anwendungen angezeigt wird.<br/> |
| *Showinshell*         | **REG \_ DWORD**     | Optionaler Parameter, der angibt, ob das Gerät in Windows-Explorer angezeigt werden soll. Der Wert 1 gibt an, dass das Gerät in Windows-Explorer angezeigt werden soll. Weitere Informationen finden Sie unter [Anforderungen für tragbare Audioplayer werden im Windows-Explorer angezeigt](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *Useextendedwmdm*     | **REG \_ DWORD**     | Ein optionaler Parameter, der Windows Media-Device Manager benachrichtigt, dass der Dienstanbieter **IMDSPDevice3**, **IMDSPObject2** und **IMDSPStorage4** unterstützt. Ohne dieses Flag werden diese Schnittstellen von Windows Media Device Manager nie aufgerufen. Der Wert 1 gibt an, dass diese Schnittstellen unterstützt werden.<br/> Dieses Flag ist für Dienstanbieter erforderlich, die mit Windows Media Player synchronisieren. (Siehe [Aktivieren der Synchronisierung mit Windows Media Player](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

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

[**IMDServiceProvider2:: kreatedevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Iwmdmdevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





