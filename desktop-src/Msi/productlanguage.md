---
description: Die ProductLanguage-Eigenschaft gibt die Sprache an, die das Installationsprogramm für zeichenfolgen in der Benutzeroberfläche verwenden soll, die nicht in der Datenbank erstellt werden.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: ProductLanguage-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd2a079767b1e39f07bdcf90f2a359604d89ccf9e394d2695b5aa74cc9e459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376455"
---
# <a name="productlanguage-property"></a>ProductLanguage-Eigenschaft

Die **ProductLanguage-Eigenschaft** gibt die Sprache an, die das Installationsprogramm für zeichenfolgen in der Benutzeroberfläche verwenden soll, die nicht in der Datenbank erstellt werden. Diese Eigenschaft muss ein numerischer Sprachbezeichner (LANGID) sein. Wenn eine Transformation die Sprache der Benutzeroberfläche in der Datenbank ändert, sollte auch der Wert dieser Eigenschaft geändert werden, um die neue Sprache widerzuspiegeln.

Diese Eigenschaft ist REQUIRED.

## <a name="remarks"></a>Hinweise

Der Wert der **ProductLanguage-Eigenschaft** muss eine der Sprachen sein, die in der [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) aufgeführt sind.

Legen Sie beim Erstellen eines Pakets als sprachneutral die **ProductLanguage-Eigenschaft** auf 0 fest, und verwenden Sie die Schriftart MS Shell Dlg als Textstil für alle geschriebenen Dialoge. Da einige Schriftarten nicht alle Zeichensätze unterstützen, können Sie mit dieser Schriftart sicherstellen, dass der Text in allen lokalisierten Versionen des Betriebssystems ordnungsgemäß angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




