---
description: Die ProductCode-Eigenschaft ist ein eindeutiger Bezeichner für die jeweilige Produktversion, der als Zeichenfolgen-GUID dargestellt wird, z. B. &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753910"
---
# <a name="productcode-property"></a>ProductCode-Eigenschaft

Die **ProductCode-Eigenschaft** ist ein eindeutiger Bezeichner für die jeweilige Produktversion, dargestellt als Zeichenfolgen-GUID, z.B. " [](guid.md) {12345678-1234-1234-1234-123456789012} ". Die in dieser GUID verwendeten Buchstaben müssen groß geschrieben werden. Diese ID muss für verschiedene Versionen und Sprachen variieren.

Ein Produktupgrade, das ein Produkt in ein völlig neues Produkt aktualisiert, muss auch den Produktcode ändern. Den 32-Bit- und 64-Bit-Versionen des Pakets einer Anwendung müssen unterschiedliche Produktcodes zugewiesen werden.

**Der ProductCode** wird als Produkteigenschaft angekündigt und ist die primäre Methode zum Angeben des Produkts. Diese Eigenschaft ist REQUIRED.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




