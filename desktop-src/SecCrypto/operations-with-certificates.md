---
description: CryptoAPI bietet Funktionen zum Arbeiten mit Zertifikaten, Zertifikat Sperr Listen (CRLs) und Zertifikat Vertrauens Listen (CTLs).
ms.assetid: 23460329-44ed-4bcb-9727-5c841070f093
title: Vorgänge mit Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2f9f5d6d541b452741f2e4634752b979f26107
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867396"
---
# <a name="operations-with-certificates"></a>Vorgänge mit Zertifikaten

[*CryptoAPI*](../secgloss/c-gly.md) bietet Funktionen zum Arbeiten mit [*Zertifikaten*](../secgloss/c-gly.md), [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs). Hierzu gehören Funktionen zum Umrechnen von codierten Typen in Kontext Typen, Funktionen, die Objekte duplizieren, und Funktionen, die diese Objekte freigeben. Diese Funktionen codieren Informationen in Kontexte, fügen diesen Kontext jedoch keinem Speicher hinzu. Diese Funktionen sind [**certkreatecertifitorecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), [**certkreatecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)und [**certkreatectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext). Verwenden Sie die entsprechende certfree-Funktion zum Freigeben von Kontexten, die von einer dieser Funktionen erstellt wurden.

Die CryptoAPI-Funktionen zum Duplizieren von Zertifikaten, CRLs und CTLs erhöhen den [*Verweis Counter*](../secgloss/r-gly.md) im angegebenen Kontext und geben einen Zeiger auf den Kontext zurück. Die duplizierenden Funktionen weisen keinen zusätzlichen Speicherplatz auf oder kopieren die Daten aus einem Kontext in einen neuen Speicherort. Diese Funktionen sind [**certduplierecertifierecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext), [**certduplierecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)und [**certduplierectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext). Mit einer dieser Funktionen erstellte Kontexte müssen mithilfe der entsprechenden certfree-Funktion freigegeben werden.

Die CryptoAPI-Funktionen, mit denen Zertifikate, CRLs und CTLs freigegeben werden, sind [**certfreecertifitorecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**certfreecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)und [**certfreectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext). Jede dieser Funktionen verringert den [*Verweis Zähler*](../secgloss/r-gly.md) in einem Kontext. Wenn der Verweis Zähler Null erreicht, wird der für den Kontext zugewiesene Arbeitsspeicher freigegeben.

Eine vollständige Liste der Funktionen für das Arbeiten mit Zertifikaten, CRLs und CTLs finden Sie unter [Zertifikat-und Zertifikat Speicher-Wartungsfunktionen](cryptography-functions.md), [Zertifikat Funktionen](cryptography-functions.md), Funktionen für die [Zertifikat Sperr Liste](cryptography-functions.md)und Funktionen für die [Zertifikat Vertrauens Liste](cryptography-functions.md).

 

 
