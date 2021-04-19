---
description: Die ProductCode-Eigenschaft ist ein eindeutiger Bezeichner für die jeweilige Produktversion, die als Zeichen folgen-GUID dargestellt wird, z \# . b. &0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372631"
---
# <a name="productcode-property"></a>ProductCode-Eigenschaft

Die **ProductCode** -Eigenschaft ist ein eindeutiger Bezeichner für die jeweilige Produktversion, die als Zeichen folgen- [GUID](guid.md)dargestellt wird, z {12345678-1234-1234-1234-123456789012} . b. "". Die in dieser GUID verwendeten Buchstaben müssen in Großbuchstaben angegeben werden. Diese ID muss für verschiedene Versionen und Sprachen variieren.

Bei einem Produkt Upgrade, bei dem ein Produkt in ein völlig neues Produkt aktualisiert wird, muss auch der Produktcode geändert werden. Den 32-Bit-und 64-Bit-Versionen des Pakets einer Anwendung müssen unterschiedliche Produktcodes zugewiesen werden.

**ProductCode** wird als Produkt Eigenschaft angekündigt und ist die primäre Methode zum Angeben des Produkts. Diese Eigenschaft ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




