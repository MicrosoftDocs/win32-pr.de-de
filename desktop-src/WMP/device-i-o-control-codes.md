---
title: Geräte-e/a-Steuerungs Codes
description: Geräte-e/a-Steuerungs Codes
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, e/a-Steuerungs Codes für Geräte
- Windows Media Player, Steuerungs Codes
- Windows Media-Device Manager
- Geräte-e/a-Steuerungs Codes
- Steuerungs Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339218"
---
# <a name="device-io-control-codes"></a>Geräte-e/a-Steuerungs Codes

Windows Media Player 10 oder höher definiert Windows Media Device Manager Geräte-e/a-Steuerungs Codes. Die folgende Tabelle enthält die Steuercodes und ihre Beschreibungen.



| E/a-Steuerungs Code                      | Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Roundtrip für IOCTL- \_ WMP- \_ Metadaten \_ \_** | 0x31504d57 | Verwaltet die Übertragung von Informationen zu Änderungen, die an Metadatenwerte aufgetreten sind. Siehe [Geräte Erweiterungen für die beschleunigte metadatenübertragung](device-extensions-for-accelerated-metadata-transfer.md).                                                                                                                                                                          |
| **IOCTL- \_ WMP- \_ Gerät \_ kann \_ synchronisiert werden**     | 0x32504d57 | Gibt an, ob ein tragbares Gerät automatische Synchronisierung unterstützt. Windows Media Player 10 oder höher bietet keinen Eingabepuffer. Der Ausgabepuffer muss einen **DWORD** -Wert zurückgeben. Der Wert 1 bedeutet, dass das Gerät die Synchronisierung unterstützt. Der Wert 0 bedeutet, dass das Gerät die automatische Synchronisierung nicht unterstützt.<br/> Weitere Informationen finden Sie unter Hinweise.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Steuerungs Codes sind in wmpdevices. h definiert.

Wenn das Gerät das **IOCTL- \_ WMP- \_ Gerät \_ \_ synchronisieren kann**, wird von Windows Media Player 10 oder höher davon ausgegangen, dass das Gerät die automatische Synchronisierung unterstützt. Beachten Sie, dass bei diesem Wert die automatische Synchronisierung nicht zulässig ist. es gibt jedoch zusätzliche Kriterien, die bestimmen, ob das Gerät die automatische Synchronisierung unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräte Erweiterungen für die beschleunigte metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





