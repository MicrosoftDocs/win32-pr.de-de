---
title: Do-Strukturen und Unions
description: Die Schnittstellen für die Übermittlungs Optimierung (Do) verwenden die folgenden Strukturen.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 860672e72e1e5f134382fd46cd9b36d1d411361e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102018"
---
# <a name="do-structures-and-unions"></a>Do-Strukturen und Unions

Die [Schnittstellen](do-interfaces.md) für die Übermittlungs Optimierung (Do) verwenden die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | Die **BG_FILE_PROGRESS** -Struktur liefert Datei bezogene Statusinformationen, wie z. b. die Anzahl der übertragenen Bytes. |
| [**BG_FILE_RANGE**](bg-file-range.md) | Die **BG_FILE_RANGE** -Struktur identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | Die **BG_JOB_PROGRESS** Struktur bietet auftragsbezogene Statusinformationen, wie z. b. die Anzahl von Bytes und übertragenen Dateien. Bei Uploadaufträgen gilt der Fortschritt für die Uploaddatei, nicht für die Antwortdatei.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | Die **BG_JOB_TIMES** -Struktur stellt auftragsbezogene Zeitstempel bereit. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | Die **BITS_FILE_PROPERTY_VALUE** Union stellt den Eigenschafts Wert der do-Datei auf Grundlage eines Werts aus der [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) Enumeration bereit. |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | Die **BITS_JOB_PROPERTY_VALUE** Union stellt den Eigenschafts Wert des Do-Auftrags basierend auf dem Wert der [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) -Enumeration bereit. |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Wird von **idomanager:: enumdownloads** verwendet, um die Downloads-Enumeration nach dem Wert der bestimmten Eigenschaft zu filtern. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifiziert einen einzelnen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Gibt ein Array von Byte Bereichen an, das aus einer Datei heruntergeladen werden soll. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Dient zum Abrufen des Status eines bestimmten Downloads. |
| [**Doswarmstats**](doswarmstats.md) | Enthält Felder für das herunterladen und Hochladen von Statistiken für eine Datei. |