---
description: Die Page Count Summary -Eigenschaft enthält die mindestens erforderliche Installationsprogrammversion des Installationspakets.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Page Count Summary -Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f19db5b8b4dc4dff3c3eb30f616803754bfac199a3aa1e6656da0f1e3fa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145413"
---
# <a name="page-count-summary-property"></a>Page Count Summary -Eigenschaft

Die Page **Count Summary** -Eigenschaft enthält die mindestens erforderliche Installationsprogrammversion des Installationspakets. Für mindestens Windows Installer 2.0 muss diese Eigenschaft auf die ganze Zahl 200 festgelegt werden. Für mindestens Windows Installer 3.0 muss diese Eigenschaft auf die ganze Zahl 300 festgelegt werden. Für mindestens Windows Installer 3.1 muss diese Eigenschaft auf 301 festgelegt werden. Für mindestens Windows Installer 4.5 muss diese Eigenschaft auf 405 festgelegt werden. Für mindestens Windows Installer 5.0 muss diese Eigenschaft auf 500 festgelegt werden.

Für [64-Bit-Windows-Installerpakete](64-bit-windows-installer-packages.md)muss diese Eigenschaft auf die ganze Zahl 200 oder höher festgelegt werden. Für 64-Bit-Windows-Installerpakete auf der Arm64-Plattform muss diese Eigenschaft auf die ganze Zahl 500 oder höher festgelegt werden.

Für ein Transformationspaket enthält die Page **Count Summary-Eigenschaft** die mindestens erforderliche Installationsprogrammversion, um die Transformation zu verarbeiten. Legen Sie auf den größeren der beiden Page **Count Summary-Eigenschaftswerte** fest, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden.

Für ein Patchpaket wird die Page **Count Summary-Eigenschaft** auf NULL festgelegt.

Diese Zusammenfassungseigenschaft ist erforderlich.

Diese Eigenschaft kann verwendet werden, um ein Paket zu erstellen, das nur mit der angegebenen Mindestversion oder einer neueren Version des Windows Installers installiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




