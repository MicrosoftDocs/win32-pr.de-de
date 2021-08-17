---
description: Die CHString-Klasse macht die folgenden Methoden verfügbar.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: CHString-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d15726702177aa484a070cca3ec1aab56d708b57991d3ff6a7aae43b1ccf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556955"
---
# <a name="chstring-methods"></a>CHString-Methoden

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Die [**CHString-Klasse**](chstring.md) macht die folgenden Methoden verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**AllocSysString-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**CHString-Konstruktoren**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Collate-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**CompareNoCase-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Leere Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Suchen nach Methoden**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**FindOneOf-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Formatieren von Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**FormatMessageW-Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**FormatV-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**FreeExtra-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**GetAllocLength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**GetAt-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**GetBufferSetLength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**GetData-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**GetLength-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**LoadStringW-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**LockBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**MakeLower-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**MakeReverse-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**MakeUpper-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Mid-Methoden**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**\[ \] Operatormethode**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString::operator+**](chstring--operator-plus.md)
-   [**CHString::operator+=**](chstring--operator-plus-equal.md)
-   [**CHString::operator=**](chstring--operator-equal.md)
-   [**operator==(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**operator==(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**operator>(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**operator>(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**operator>=(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**operator>=(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**operator<(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**operator<(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**operator<=(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**operator<=(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**operator!=(constCHString&, constCHString&)-Methode**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**operator!=(constCHString&, constLPCWSTR&)-Methode**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Operator LPCWSTR-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**ReleaseBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**ReverseFind-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Rechte Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**SetAt-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**SpanExcluding-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**SpanIncluding-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**TrimLeft-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**TrimRight-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**UnlockBuffer-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
