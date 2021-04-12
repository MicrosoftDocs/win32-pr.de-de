---
title: Unicode und ANSI-Zeichen folgen werden umgerechnet
description: Microsoft Active Accessibility verwendet gemäß dem BSTR-Datentyp definierte Unicode-Zeichen folgen.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315783"
---
# <a name="converting-unicode-and-ansi-strings"></a>Unicode und ANSI-Zeichen folgen werden umgerechnet

Microsoft Active Accessibility verwendet gemäß dem **BSTR** -Datentyp definierte Unicode-Zeichen folgen. Wenn Ihre Anwendung keine Unicode-Zeichen folgen verwendet, oder wenn Sie Zeichen folgen für bestimmte API-Aufrufe konvertieren möchten, verwenden Sie die Microsoft Win32-Funktionen [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) , um die erforderliche Konvertierung auszuführen.

Verwenden Sie [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) , um eine Unicode-Zeichenfolge in eine ANSI-Zeichenfolge zu konvertieren. Die [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion konvertiert eine ANSI-Zeichenfolge in eine Unicode-Zeichenfolge.

Verwenden Sie [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) und [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) , um **BSTR** -Datentypen zuzuordnen und freizugeben.

Weitere Informationen zu diesen Zeichen folgen Funktionen finden Sie unter ihren Verweisen im Windows Software Development Kit (SDK).

 

 