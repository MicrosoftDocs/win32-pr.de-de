---
description: In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema idefault- \* Konstanten definiert.
ms.assetid: 4fa8b5f3-8c01-44fb-b6fd-8dbf38e3d361
title: LOCALE_IDEFAULT *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9c440c27a2fe551eae7d03d66cc43b500e8f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346478"
---
# <a name="locale_idefault-constants"></a>Gebiets Schema- \_ idefault- \* Konstanten

In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema idefault- \* Konstanten definiert.



| Wert                          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gebiets Schema \_ idefaultansicodepage   | Die ANSI-Codepage, die von einem Gebiets Schema für Anwendungen verwendet wird, die Unicode nicht unterstützen. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist sechs, einschließlich eines abschließenden NULL-Zeichens. Wenn keine ANSI-Codepage verfügbar ist, kann nur Unicode für das Gebiets Schema verwendet werden. In diesem Fall ist der Wert CP \_ ACP (0). Ein solches Gebiets Schema kann nicht als System Gebiets Schema festgelegt werden. Anwendungen, die Unicode nicht unterstützen, funktionieren nicht ordnungsgemäß mit Gebiets Schemas, die als "nur Unicode" gekennzeichnet sind. Eine Liste der ANSI-und anderen Codepages finden Sie unter [Code Page Identifier](code-page-identifiers.md). |
| Gebiets Schema \_ idefehlercodepage       | OEM-Codepage (Original Equipment Manufacturer), die dem Land bzw. der Region zugeordnet ist. Die OEM-Codepage wird für die Konvertierung von MS-DOS-basierten Anwendungen im Textmodus verwendet. Wenn das Gebiets Schema keine OEM-Codepage verwendet, ist der Wert CP \_ oemcp (1). Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist sechs, einschließlich eines abschließenden NULL-Zeichens. Eine Liste der OEM-und anderen Codepages finden Sie unter [Code Page Identifier](code-page-identifiers.md).                                                                                                               |
| Gebiets Schema \_ idefehlerland        | Veraltet. Darf nicht verwendet werden. Dieser Wert wurde bereitgestellt, damit teilweise angegebene Gebiets Schemas mit Standardwerten abgeschlossen werden können. Teilweise angegebene Gebiets Schemas sind nun veraltet.                                                                                                                                                                                                                                                                                                                                                                                               |
| Gebiets \_ Schema idefaultebcdicodepage | **Windows 2000:** Standardmäßige Extended Binary Coded Decimal Interchange Code (EBCDIC)-Codepage, die dem Gebiets Schema zugeordnet ist. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist sechs, einschließlich eines abschließenden NULL-Zeichens. Eine Liste von EBCDIC und anderen Codepages finden Sie unter [Code Page Identifier](code-page-identifiers.md).                                                                                                                                                                                                                                     |
| Gebiets Schema \_ idefehlersprache       | Veraltet. Darf nicht verwendet werden. Dieser Wert wurde bereitgestellt, damit teilweise angegebene Gebiets Schemas mit Standardwerten abgeschlossen werden können. Teilweise angegebene Gebiets Schemas sind nun veraltet.                                                                                                                                                                                                                                                                                                                                                                                               |
| Gebiets Schema \_ idefehlermaccodepage    | Standardmäßige Macintosh-Codepage, die dem Gebiets Schema zugeordnet ist. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist sechs, einschließlich eines abschließenden NULL-Zeichens. Wenn das Gebiets Schema keine Macintosh-Codepage verwendet, ist der Wert CP \_ MACCP (2). Eine Liste der Macintosh-(Mac) und anderen Codepages finden Sie unter [Code Page Identifier](code-page-identifiers.md).                                                                                                                                                                                                              |



 

 

 



