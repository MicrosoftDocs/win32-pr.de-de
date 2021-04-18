---
description: 'Wenn sich das Installationspaket, das mit einer Anwendung ausgeliefert wird, nicht im Stammverzeichnis der CD-ROM befindet, die Kunden empfängt, muss die mediapackagepath-Eigenschaft in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-Rom festgelegt werden. Wenn z. b. der Pfad zum Paket auf dem Medium "E: \\ myPath \\My.msi lautet, verwenden Sie mediapackagepath =&\# 0034; \\ MyPath \\ & \# 0034;. Administratoren können CD-ROMs von einem administrativen Installations Punkt aus erstellen. Wenn der Speicherort des Stamm Verzeichnisses der Installation auf den neuen CD-ROMs geändert wird, muss die mediapackagepath-Eigenschaft auf den neuen Pfad festgelegt werden, der von diesem Medium aus installiert werden soll. Eine Quelle mit einem anderen Speicherort auf der CD-Rom ist nicht verwendbar. Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen administrativen Installations Punkt von einem Versand Medium erstellen.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Mediapackagepath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360896"
---
# <a name="mediapackagepath-property"></a>Mediapackagepath (Eigenschaft)

Wenn sich das Installationspaket, das mit einer Anwendung ausgeliefert wird, nicht im Stammverzeichnis der CD-ROM befindet, die Kunden empfängt, muss die **mediapackagepath** -Eigenschaft in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-Rom festgelegt werden.

Wenn z. b. der Pfad zum Paket auf dem Medium "E: \\ myPath \\My.msi lautet, verwenden Sie mediapackagepath =" \\ myPath \\ ".

Administratoren können CD-ROMs von einem administrativen Installations Punkt aus erstellen. Wenn der Speicherort des Stamm Verzeichnisses der Installation auf den neuen CD-ROMs geändert wird, muss die **mediapackagepath** -Eigenschaft auf den neuen Pfad festgelegt werden, der von diesem Medium aus installiert werden soll. Eine Quelle mit einem anderen Speicherort auf der CD-Rom ist nicht verwendbar. Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen administrativen Installations Punkt von einem Versand Medium erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




