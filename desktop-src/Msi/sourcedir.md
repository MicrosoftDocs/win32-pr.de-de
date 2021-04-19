---
description: Die SourceDir-Eigenschaft ist das Stammverzeichnis, das die CAB-Quelldatei oder die Quelldatei Struktur des Installationspakets enthält. Dieser Wert wird für die Verzeichnis Auflösung verwendet.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372720"
---
# <a name="sourcedir-property"></a>SourceDir-Eigenschaft

Die **SourceDir** -Eigenschaft ist das Stammverzeichnis, das die CAB-Quelldatei oder die Quelldatei Struktur des Installationspakets enthält. Dieser Wert wird für die Verzeichnis Auflösung verwendet.

## <a name="default-value"></a>Standardwert

Das Verzeichnis, in dem das Installationspaket enthalten ist.

## <a name="remarks"></a>Bemerkungen

Die [ResolveSource-Aktion](resolvesource-action.md) muss aufgerufen werden, bevor **die SourceDir** -Eigenschaft in einem Ausdruck verwendet wird, oder es wird versucht, den Wert von **SourceDir** mit [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)abzurufen. Die Aktion "ResolveSource" sollte nicht ausgeführt werden, während die Quelle nicht verfügbar ist, z. b. beim Deinstallieren einer Anwendung, da dies zu einer unbeabsichtigten Aufforderung für das Quell Medium führen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




