---
description: Der Installer legt die SystemFolder-Eigenschaft auf den vollständigen Pfad des System Ordners fest.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366781"
---
# <a name="systemfolder-property"></a>SystemFolder-Eigenschaft

Der Installer legt die **SystemFolder** -Eigenschaft auf den vollständigen Pfad des System Ordners fest.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird vom Installationsprogramm festgelegt. Beispielsweise kann auf 32-Bit-Fenstern der Wert "C: \\ Windows \\ system32" lauten. Auf 64-Bit-Fenstern kann der Wert "C: \\ Windows \\ syswow64" lauten.

Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows-Ordners. Sie befindet sich jedoch auf einem Server, wenn Sie für freigegebene Fenster konfiguriert ist.

Dieser Ordner ist lokal, auch wenn er für freigegebene Fenster konfiguriert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




