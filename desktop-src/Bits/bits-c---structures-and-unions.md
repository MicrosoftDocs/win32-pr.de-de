---
title: Bits-Strukturen und Unions
description: Die Background Intelligent Transfer Service (Bits)-Schnittstellen verwenden die folgenden Strukturen.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 93763daa73bc96e12dd27b862d75fbb23869c20f
ms.sourcegitcommit: 31f494fef71b63ad411b86b22b4cc01af6e37c8d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2019
ms.locfileid: "104311663"
---
# <a name="bits-structures-and-unions"></a>Bits-Strukturen und Unions

Die Background Intelligent Transfer Service (Bits)- [Schnittstellen](bits-interfaces.md) verwenden die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifiziert das Ziel (Proxy oder Server), das Authentifizierungsschema und die Anmelde Informationen des Benutzers, die für Benutzer Authentifizierungsanforderungen verwendet werden sollen. Die-Struktur wird an die [IBackgroundCopyJob2:: Set-Anmelde](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)Informationen-Methode übermittelt. |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifiziert die Anmelde Informationen, die für das in der [BG_AUTH_CREDENTIALS Struktur](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials)angegebene Authentifizierungsschema verwendet werden sollen. |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifiziert den Benutzernamen und das Kennwort für die Authentifizierung. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Stellt die lokalen und Remote Namen der zu übertragenden Datei bereit. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Stellt Datei bezogene Statusinformationen bereit, z. b. die Anzahl der übertragenen Bytes. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Stellt auftragsbezogene Statusinformationen bereit, wie z. b. die Anzahl von Bytes und übertragenen Dateien. Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei. Informationen zum Anzeigen des Status der Antwortdatei finden Sie in der [BG_JOB_REPLY_PROGRESS-Struktur](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Stellt Statusinformationen im Zusammenhang mit dem Antwort Teil eines Upload-Antwort-Auftrags bereit. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Stellt auftragsbezogene Zeitstempel bereit. |
| [**BITS_FILE_PROPERTY_VALUE Union**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Stellt den Eigenschafts Wert einer Bits-Datei bereit. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Gibt den Eigenschafts Wert des Bits-Auftrags basierend auf dem Wert der [BITS_JOB_PROPERTY_ID Enumeration](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)an. |
