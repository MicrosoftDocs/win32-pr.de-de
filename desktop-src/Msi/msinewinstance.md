---
description: Die msinewinstance-Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit instanztransformationen an.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Msinewinstance (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373856"
---
# <a name="msinewinstance-property"></a>Msinewinstance (Eigenschaft)

Die **msinewinstance** -Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit instanztransformationen an. Diese Eigenschaft unterstützt mehrere Instanzen durch Produktcode – veränderliche Transformationen. Der Wert dieser Eigenschaft ist 1. Wenn diese Eigenschaft in der Befehlszeile vorhanden ist, muss auch die [**Transformationen**](transforms.md) -Eigenschaft vorhanden sein. Die erste in **Transformationen** aufgelistete Transformation muss eine instanztransformation sein. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md) .

Diese Eigenschaft ist für das Installationsprogramm verfügbar, das ein System in Windows Server 2003 oder Windows XP ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




