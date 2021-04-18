---
description: Der Installer legt die System64Folder-Eigenschaft auf den vollständigen Pfad zum vordefinierten System64-Ordner fest. Die vorhandene System64Folder-Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371535"
---
# <a name="system64folder-property"></a>System64Folder-Eigenschaft

Der Installer legt die **System64Folder** -Eigenschaft auf den vollständigen Pfad zum vordefinierten System64-Ordner fest. Die vorhandene **System64Folder** -Eigenschaft wird auf den entsprechenden 32-Bit-Ordner festgelegt.

## <a name="remarks"></a>Bemerkungen

Das Installationsprogramm legt diese Eigenschaft auf 64-Bit-Fenstern fest. Beispielsweise kann auf 64-Bit-Fenstern der Wert C: \\ Fenster System32 lauten \\ . Diese Eigenschaft wird auf 32-Bit-Fenstern nicht verwendet.

Dieser Ordner ist normalerweise ein Unterverzeichnis des Windows-Ordners. Sie befindet sich jedoch auf einem Server, wenn Sie für freigegebene Fenster konfiguriert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




