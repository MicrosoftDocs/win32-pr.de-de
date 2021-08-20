---
description: Das Installationsprogramm legt die SystemFolder-Eigenschaft auf den vollständigen Pfad des Ordners System fest.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1567942e981af161654d41988ef797b64116af5cdb25e07a3d4f1465fc4ce975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142008"
---
# <a name="systemfolder-property"></a>SystemFolder-Eigenschaft

Das Installationsprogramm legt die **SystemFolder-Eigenschaft** auf den vollständigen Pfad des Ordners System fest.

## <a name="remarks"></a>Hinweise

Das Installationsprogramm legt diese Eigenschaft fest. Bei 32-Bit-Windows kann der Wert beispielsweise C: \\ Windows \\ System32 sein. Auf 64-Bit-Windows kann der Wert C: \\ Windows \\ SysWow64 sein.

Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows Ordners. Er befindet sich jedoch auf einem Server, wenn er für Freigegebene Windows konfiguriert ist.

Dieser Ordner ist lokal, auch wenn er für freigegebene Windows konfiguriert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




