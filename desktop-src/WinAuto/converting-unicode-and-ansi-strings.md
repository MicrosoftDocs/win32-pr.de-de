---
title: Konvertieren von Unicode- und ANSI-Zeichenfolgen
description: Microsoft Active Accessibility verwendet Unicode-Zeichenfolgen, wie vom BSTR-Datentyp definiert.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b001791b2de2bde4c1efa0b09dcee55203a6cf69a41d5b7927c5df5438de90fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030940"
---
# <a name="converting-unicode-and-ansi-strings"></a>Konvertieren von Unicode- und ANSI-Zeichenfolgen

Microsoft Active Accessibility verwendet Unicode-Zeichenfolgen, wie vom **BSTR-Datentyp** definiert. Wenn Ihre Anwendung keine Unicode-Zeichenfolgen verwendet oder Zeichenfolgen für bestimmte API-Aufrufe konvertieren möchten, verwenden Sie die Microsoft Win32-Funktionen [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte,**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) um die erforderliche Konvertierung durchzuführen.

Verwenden [**Sie WideCharToMultiByte,**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) um eine Unicode-Zeichenfolge in eine ANSI-Zeichenfolge zu konvertieren. Die [**MultiByteToWideChar-Funktion**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) konvertiert eine ANSI-Zeichenfolge in eine Unicode-Zeichenfolge.

Verwenden [**Sie SysAllocString und**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) [**SysFreeString,**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) um **BSTR-Datentypen** zu zuordnen und frei zu geben.

Weitere Informationen zu diesen Zeichenfolgenfunktionen finden Sie im Windows Software Development Kit (SDK).

 

 