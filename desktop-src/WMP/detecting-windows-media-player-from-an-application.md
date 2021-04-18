---
title: Erkennen von Windows-Media Player aus einer Anwendung
description: Erkennen von Windows-Media Player aus einer Anwendung
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, erkennen von Anwendungen
- Erkennen von Windows-Media Player aus Anwendungen
- Registrierung, erkennen von Windows-Media Player aus Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337809"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Erkennen von Windows-Media Player aus einer Anwendung

Sie können ermitteln, welche Version von Windows Media Player installiert ist, indem Sie den folgenden Registrierungsschlüssel überprüfen:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Active Setup \\ installierte Komponenten**

Informationen zu Windows Media Player 6,4 finden Sie unter Key **{22d6f 312-b0f 6-11D0-94ab-0080c74c7e95}**.

Informationen zu Windows Media Player 7 oder höher finden Sie unter Key **{6BF 52a52-394a-11d3-b153-00c04f 79faa6}**.

Unter einem dieser Schlüssel, wenn die **isinstemstation**<dl> <dt>

Datentyp
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Datentyp
</dt> <dd>Zeichenfolge</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Neuverteilen von Windows Media Player-Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




