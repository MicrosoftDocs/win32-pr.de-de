---
title: BITS-Strukturen und -Unions
description: Die Background Intelligent Transfer Service -Schnittstellen (BITS) verwenden die folgenden Strukturen.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 199d5648ba8205d0417304350a104b2e16a607e4d7f1bdce4dfe9ecec34f98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702030"
---
# <a name="bits-structures-and-unions"></a>BITS-Strukturen und -Unions

Die Background Intelligent Transfer Service -Schnittstellen [(BITS)](bits-interfaces.md) verwenden die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifiziert das Ziel (Proxy oder Server), das Authentifizierungsschema und die Anmeldeinformationen des Benutzers, die für Benutzerauthentifizierungsanforderungen verwendet werden. Die -Struktur wird an die [IBackgroundCopyJob2::SetCredentials-Methode übergeben.](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifiziert die Anmeldeinformationen, die für das in der -Struktur angegebene Authentifizierungsschema [BG_AUTH_CREDENTIALS werden.](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifiziert den Benutzernamen und das Kennwort für die Authentifizierung. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Stellt die lokalen und Remotenamen der datei, die übertragen werden soll. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Stellt dateibezogene Statusinformationen wie die Anzahl der übertragenen Bytes zur Verfügung. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifiziert einen Bytebereich, der aus einer Datei heruntergeladen werden soll. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Stellt auftragsbezogene Statusinformationen wie die Anzahl der übertragenen Bytes und Dateien zur Verfügung. Bei Uploadaufträgen gilt der Status nicht für die Antwortdatei, sondern für die Uploaddatei. Informationen zum Anzeigen des Status der Antwortdatei finden Sie in [der BG_JOB_REPLY_PROGRESS Struktur](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Stellt Statusinformationen im Zusammenhang mit dem Antwortteil eines Upload-Antwort-Auftrags zur Verfügung. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Stellt auftragsbezogene Zeitstempel zur |
| [**BITS_FILE_PROPERTY_VALUE Union**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Stellt den -Eigenschaftswert einer BITS-Datei zur |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Stellt den -Eigenschaftswert des BITS-Auftrags basierend auf dem Wert der BITS_JOB_PROPERTY_ID [-Enumeration zur](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id) |
