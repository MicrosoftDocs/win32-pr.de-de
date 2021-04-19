---
description: Die msihiddenproperties-Eigenschaft kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kenn Wörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Msihiddenproperties (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355933"
---
# <a name="msihiddenproperties-property"></a>Msihiddenproperties (Eigenschaft)

Die **msihiddenproperties** -Eigenschaft kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kenn Wörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt. Um zu verhindern, dass eine Eigenschaft in die Protokolldatei geschrieben wird, legen Sie den Wert der Eigenschaft **msihiddenproperties** auf den Namen der Eigenschaft fest, die Sie ausblenden möchten. Sie können mehrere Eigenschaften ausblenden, indem Sie eine Zeichenfolge von Eigenschaften Namen angeben, die durch Semikolons (;) getrennt sind.

> [!Note]  
> Wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt ist, schreibt das Installationsprogramm Informationen, die in der Befehlszeile eingegeben werden, in das Protokoll. Dadurch werden öffentliche Eigenschaften in einer Befehlszeile sichtbar, auch wenn die Eigenschaft in der **msihiddenproperties** -Eigenschaft enthalten ist. Dadurch können vertrauliche Informationen in eine Befehlszeile eingegeben werden, die im Protokoll sichtbar ist. Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




