---
description: Die MsiHiddenProperties-Eigenschaft kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kennwörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: MsiHiddenProperties-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acea21b946a4169748c96970143d6c44c6bf682ce6f6a8e4624791c52d0ba813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628105"
---
# <a name="msihiddenproperties-property"></a>MsiHiddenProperties-Eigenschaft

Die **MsiHiddenProperties-Eigenschaft** kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kennwörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt. Um zu verhindern, dass eine Eigenschaft in die Protokolldatei geschrieben wird, legen Sie den Wert der **MsiHiddenProperties-Eigenschaft** auf den Namen der Eigenschaft fest, die Sie ausblenden möchten. Sie können mehrere Eigenschaften ausblenden, indem Sie eine Zeichenfolge von Eigenschaftsnamen angeben, die durch Semikolons (;).

> [!Note]  
> Wenn die [Debugrichtlinie](debug.md) auf den Wert 7 festgelegt ist, schreibt das Installationsprogramm die in einer Befehlszeile eingegebenen Informationen in das Protokoll. Dadurch werden öffentliche Eigenschaften, die in einer Befehlszeile eingegeben werden, sichtbar, auch wenn die Eigenschaft in der **MsiHiddenProperties-Eigenschaft** enthalten ist. Dadurch können vertrauliche Informationen, die in einer Befehlszeile eingegeben wurden, im Protokoll sichtbar werden. Weitere Informationen finden Sie unter [Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden.](preventing-confidential-information-from-being-written-into-the-log-file.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




