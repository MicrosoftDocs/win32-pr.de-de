---
description: Das Installationsprogramm legt die System64Folder-Eigenschaft auf den vollständigen Pfad zum vordefinierten System64-Ordner fest. Die vorhandene System64Folder-Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500430"
---
# <a name="system64folder-property"></a>System64Folder-Eigenschaft

Das Installationsprogramm legt die **System64Folder-Eigenschaft** auf den vollständigen Pfad zum vordefinierten System64-Ordner fest. Die vorhandene **System64Folder-Eigenschaft** wird auf den entsprechenden 32-Bit-Ordner festgelegt.

## <a name="remarks"></a>Hinweise

Das Installationsprogramm legt diese Eigenschaft auf 64-Bit-Windows. Auf 64-Bit-Windows kann der Wert beispielsweise C: \\ Window \\ System32 sein. Diese Eigenschaft wird nicht auf 32-Bit-Windows.

Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows Ordners. Sie befindet sich jedoch auf einem Server, wenn sie für Freigegebene Windows.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




