---
title: Erkennen Windows Media Player aus einer Anwendung
description: Erkennen Windows Media Player aus einer Anwendung
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player,erkennen von Anwendungen
- Erkennen von Windows Media Player aus Anwendungen
- Registrierung,Erkennen Windows Media Player von Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579486"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Erkennen Windows Media Player aus einer Anwendung

Sie können ermitteln, welche Version Windows Media Player installiert ist, indem Sie den folgenden Registrierungsschlüssel überprüfen:

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Active Setup \\ Installed Components**

Für Windows Media Player 6.4 sehen Sie sich den Schlüssel **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}** an.

Für Windows Media Player 7 oder höher sehen Sie sich den Schlüssel **{6BF52A52-394A-11d3-B153-00C04F79FAA6}** an.

Unter einem dieser Schlüssel, wenn **isInstalled**<dl> <dt>

Datentyp
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Datentyp
</dt> <dd>Zeichenfolge</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verteilen Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




