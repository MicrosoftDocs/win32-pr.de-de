---
description: Die Zusammenfassungs Eigenschaft Seitenanzahl enthält die für das Installationspaket erforderliche mindestinstallerversion.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Zusammenfassungs Eigenschaft für Seitenanzahl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367674"
---
# <a name="page-count-summary-property"></a>Zusammenfassungs Eigenschaft für Seitenanzahl

Die **Zusammenfassungs Eigenschaft Seitenanzahl** enthält die für das Installationspaket erforderliche mindestinstallerversion. Für mindestens Windows Installer 2,0 muss diese Eigenschaft auf die ganze Zahl 200 festgelegt werden. Für mindestens Windows Installer 3,0 muss diese Eigenschaft auf die ganze Zahl 300 festgelegt werden. Für mindestens Windows Installer 3,1 muss diese Eigenschaft auf 301 festgelegt werden. Für mindestens Windows Installer 4,5 muss diese Eigenschaft auf 405 festgelegt werden. Für mindestens Windows Installer 5,0 muss diese Eigenschaft auf 500 festgelegt werden.

Bei [64-Bit-Windows Installer Paketen](64-bit-windows-installer-packages.md)muss diese Eigenschaft auf die ganze Zahl 200 oder höher festgelegt werden. Bei 64-Bit-Windows Installer Paketen auf der Arm64-Plattform muss diese Eigenschaft auf die ganze Zahl 500 oder höher festgelegt werden.

Bei einem Transformations Paket enthält die **Zusammenfassungs Eigenschaft Seitenanzahl** die mindestinstallerversion, die zum Verarbeiten der Transformation erforderlich ist. Legen Sie auf die größere der beiden **Zusammenfassungs** Eigenschaftswerte der Seitenanzahl fest, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden.

Bei einem Patchpaket wird die **Zusammenfassungs Eigenschaft der Seitenanzahl** auf NULL festgelegt.

Diese Zusammenfassungs Eigenschaft ist erforderlich.

Diese Eigenschaft kann verwendet werden, um ein Paket zu erstellen, das nur mit der angegebenen Mindestversion oder einer höheren Version des Windows Installer installiert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




