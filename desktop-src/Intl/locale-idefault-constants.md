---
description: In diesem Thema werden die \_ locale-IDEFAULT-Konstanten \* definiert, die von NLS verwendet werden.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: LOCALE_IDEFAULT* Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0524ea64d9924439e14ae6cb3cf16fed8a5f97ffb1e95d5f7fea98d5b6c61329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106780"
---
# <a name="locale_idefault-constants"></a>LOCALE \_ \* IDEFAULT-Konstanten

In diesem Thema werden die \_ locale-IDEFAULT-Konstanten \* definiert, die von NLS verwendet werden.



| Wert                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LOCALE \_ IDEFAULTANSICODEPAGE   | Die ANSI-Codepage, die von einem -Locale für Anwendungen verwendet wird, die Unicode nicht unterstützen. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, ist sechs, einschließlich eines beendenden NULL-Zeichens. Wenn keine ANSI-Codepage verfügbar ist, kann nur Unicode für das -Locale verwendet werden. In diesem Fall ist der Wert CP \_ ACP (0). Ein solches Locale kann nicht als System-Locale festgelegt werden. Anwendungen, die Unicode nicht unterstützen, funktionieren nicht ordnungsgemäß mit Als "nur Unicode" markierten Locals. Eine Liste der ANSI- und anderen Codepages finden Sie unter [Codepagebezeichner](code-page-identifiers.md). |
| LOCALE \_ IDEFAULTCODEPAGE       | Oem-Codepage (Original Equipment Manufacturer), die dem Land/der Region zugeordnet ist. Die OEM-Codepage wird für die Konvertierung von MS-DOS-basierten Textmodusanwendungen verwendet. Wenn das Locale keine OEM-Codepage verwendet, ist der Wert CP \_ OEMCP (1). Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, ist sechs, einschließlich eines beendenden NULL-Zeichens. Eine Liste der OEM- und anderen Codepages finden Sie unter [Codepagebezeichner](code-page-identifiers.md).                                                                                                               |
| LOCALE \_ IDEFAULTCOUNTRY        | Veraltet. Darf nicht verwendet werden. Dieser Wert wurde bereitgestellt, sodass teilweise angegebene Locales mit Standardwerten abgeschlossen werden konnten. Teilweise angegebene Locales sind jetzt veraltet.                                                                                                                                                                                                                                                                                                                                                                                               |
| LOCALE \_ IDEFAULTEBCDICCODEPAGE | **Windows 2000:** Die Extended Binary Coded Decimal Interchange Code (EBCDIC)-Standardcodepage, die dem -Locale zugeordnet ist. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, ist sechs, einschließlich eines beendenden NULL-Zeichens. Eine Liste der EBCDIC- und anderen Codepages finden Sie unter [Codepagebezeichner](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| LOCALE \_ IDEFAULTLANGUAGE       | Veraltet. Darf nicht verwendet werden. Dieser Wert wurde bereitgestellt, sodass teilweise angegebene Locales mit Standardwerten abgeschlossen werden konnten. Teilweise angegebene Locales sind jetzt veraltet.                                                                                                                                                                                                                                                                                                                                                                                               |
| LOCALE \_ IDEFAULTMACCODEPAGE    | Macintosh-Standardcodepage, die dem -Locale zugeordnet ist. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, ist sechs, einschließlich eines beendenden NULL-Zeichens. Wenn das Locale keine Macintosh-Codepage verwendet, ist der Wert CP \_ M MACINTOSH (2). Eine Liste der Macintosh-Codepages (MAC) und anderer Codepages finden Sie unter [Codepagebezeichner](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



