---
title: Geräte-E/A-Steuerungscodes
description: Geräte-E/A-Steuerungscodes
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player,Geräte-E/A-Steuerungscodes
- Windows Media Player,Steuercodes
- Windows Medien Geräte-Manager
- Geräte-E/A-Steuerungscodes
- Steuerungscodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d610b396125cf190764b53106ca6535a214e2c8166f4e69de884c113fd77ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935849"
---
# <a name="device-io-control-codes"></a>Geräte-E/A-Steuerungscodes

Windows Media Player 10 oder höher definiert Windows Media Geräte-Manager-E/A-Steuerungscodes. Die folgende Tabelle enthält die Steuerelementcodes und deren Beschreibungen.



| E/A-Steuerungscode                      | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ROUNDTRIP FÜR \_ IOCTL-WMP-METADATEN \_ \_ \_** | 0x31504d57 | Verwaltet die Übertragung von Informationen zu Änderungen, die an Metadatenwerten aufgetreten sind. Weitere Informationen [finden Sie unter Geräteerweiterungen für die beschleunigte Metadatenübertragung.](device-extensions-for-accelerated-metadata-transfer.md)                                                                                                                                                                          |
| **\_IOCTL-WMP-GERÄT \_ \_ KANN SYNCHRONISIERT \_ WERDEN**     | 0x32504d57 | Gibt an, ob ein portables Gerät die automatische Synchronisierung unterstützt. Windows Media Player 10 oder höher bietet keinen Eingabepuffer. Der Ausgabepuffer muss einen **DWORD-Wert** zurückgeben. Der Wert 1 bedeutet, dass das Gerät die Synchronisierung unterstützt. Der Wert 0 bedeutet, dass das Gerät die automatische Synchronisierung nicht unterstützt.<br/> Weitere Informationen finden Sie unter Hinweise.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Steuerungscodes werden in wmpdevices.h definiert.

Wenn das Gerät **IOCTL \_ WMP \_ DEVICE CAN \_ \_ SYNC** nicht unterstützt, wird Windows Media Player 10 oder höher davon ausgegangen, dass das Gerät die automatische Synchronisierung unterstützt. Beachten Sie, dass dieser Wert zwar die automatische Synchronisierung nicht zumuten kann, es jedoch zusätzliche Kriterien gibt, um zu bestimmen, ob das Gerät die automatische Synchronisierung unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräteerweiterungen für die beschleunigte Metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





