---
description: Die MSINEWINSTANCE-Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit Instanztransformationen an.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: MSINEWINSTANCE(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b26831f1171813d9df9e2c4124a4d6c24ea7efbf707fc5c15eefc9d6a8b1046
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082850"
---
# <a name="msinewinstance-property"></a>MSINEWINSTANCE(Eigenschaft)

Die **MSINEWINSTANCE-Eigenschaft** gibt die Installation einer neuen Instanz eines Produkts mit Instanztransformationen an. Diese Eigenschaft unterstützt mehrere Instanzen durch Änderungen am Produktcode. Der Wert dieser Eigenschaft ist 1. Wenn diese Eigenschaft in der Befehlszeile vorhanden ist, muss auch die [**TRANSFORMS-Eigenschaft**](transforms.md) vorhanden sein. Die erste in **TRANSFORMS aufgeführte Transformation muss** eine Instanztransformation sein. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md)

Diese Eigenschaft ist verfügbar, wenn das Installationsprogramm ein System auf Windows Server 2003 oder Windows XP ausgeführt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




