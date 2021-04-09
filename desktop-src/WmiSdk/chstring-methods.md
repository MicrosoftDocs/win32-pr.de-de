---
description: Die chstring-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Chstring-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042476"
---
# <a name="chstring-methods"></a>Chstring-Methoden

\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die [**chstring**](chstring.md) -Klasse stellt die folgenden Methoden zur Verfügung.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Methode ' zugeordcsysstring '**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Chstring-Konstruktoren**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**COLLATE-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Comparumocase-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Empty-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Methoden suchen**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Findoneof-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Formatieren von Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Formatmessagew-Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Formatv-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Methode "freextra"**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Getalloclength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**GetAt-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Getbuffersetlength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**GetData-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**GetLength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Loadstringw-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**LockBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Makelower-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Makereverse-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Makeuppermethode**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Mid-Methoden**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**Operator- \[ \] Methode**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**Chstring:: Operator +**](chstring--operator-plus.md)
-   [**Chstring:: Operator + =**](chstring--operator-plus-equal.md)
-   [**Chstring:: Operator =**](chstring--operator-equal.md)
-   [**Operator = = (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**Operator = = (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**Operator> (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**Operator> (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**Operator>= (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**Operator>= (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**Operator< (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**Operator< (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**Operator<= (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**Operator<= (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**Operator! = (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**Operator! = (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Operator LPCWSTR-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**ReleaseBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Reverdie Find-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Right-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Methode "-Methode"**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Span Ausschluss-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Span-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**TrimLeft-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**TrimRight-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**UnlockBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
