---
title: Registrierungs Reflektion
description: Der Registrierungs Redirector isoliert 32-Bit-und 64-Bit-Anwendungen, indem er separate logische Sichten bestimmter Teile der Registrierung auf WOW64 bereitstellt. Allerdings müssen die Werte einiger Registrierungsschlüssel in den 32-Bit-und 64-Bit-Sichten identisch sein.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- Registrierungs Reflektion 64-Bit-Windows-Programmierung
- Reflektion 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337445"
---
# <a name="registry-reflection"></a>Registrierungs Reflektion

\[Die Informationen in diesem Thema gelten für Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP. Ab Windows 7 und Windows Server 2008 R2 verwendet WOW64 nicht mehr die Registrierungs Reflektion, und früher reflektierte Schlüssel werden stattdessen freigegeben. Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md).\]

Der [Registrierungs Redirector](registry-redirector.md) isoliert 32-Bit-und 64-Bit-Anwendungen, indem er separate logische Sichten bestimmter Teile der Registrierung auf WOW64 bereitstellt. Allerdings müssen die Werte einiger Registrierungsschlüssel in den 32-Bit-und 64-Bit-Sichten identisch sein.

Der Prozess der *Registrierungs Reflektion* kopiert Registrierungsschlüssel und-Werte zwischen zwei Registrierungs Sichten, um sie synchron zu halten. Jede Ansicht verfügt über eine separate physische Kopie jedes reflektierten Registrierungsschlüssels, eine für die 32-Bit-Registrierungs Ansicht und die andere für die 64-Bit-Registrierungs Ansicht.

Eine reflektierte Taste wird kopiert, wenn eine Taste durch Aufrufen von [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)geschlossen wird. Beachten Sie, dass dies zu einer möglichen Racebedingung führt: Wenn der reflektierte Schlüssel von mehr als einem Prozess geändert wird, bestimmt der letzte **RegCloseKey** -Rückruf den endgültigen Wert des Schlüssels.

Der Reflektor kopiert com-Aktivierungsdaten für lokale Server zwischen den Sichten, kopiert jedoch keine Prozess internen Daten, 32/64 da eine Prozess interne Daten Mischung in 64-Bit-Fenstern nicht zulässig ist.

Die Reflektion ist nicht für freigegebene Registrierungsschlüssel oder für Registrierungsschlüssel aktiviert, die nicht umgeleitet werden. Beispielsweise ist die Reflektion für den **System Schlüssel des \_ lokalen \_ \\ HKEY** -Computers nicht aktiviert. Eine Liste der Registrierungsschlüssel, die umgeleitet, freigegeben oder reflektiert werden, finden Sie unter [von WOW64 betroffene Registrierungsschlüssel](shared-registry-keys.md).

Die Registrierungs Reflektion verwendet eine "Last Writer WINS"-Richtlinie, wie im folgenden Beispiel veranschaulicht:

-   Nach einer Neuinstallation von 64-Bit-Windows wird 64-Bit-Wordpad.exe für die Verarbeitung von doc-Dateien registriert. Der Reflektor kopiert die doc-Registrierung aus der 64-Bit-Registrierungs Ansicht in die 32-Bit-Registrierungs Ansicht.
-   Ein Administrator installiert 32-Bit-Office, das 32-Bit-Winword.exe registriert, um doc-Dateien in der 32-Bit-Registrierungs Ansicht zu verarbeiten. Der Registrierungs Reflektor kopiert diese Informationen in die 64-Bit-Registrierungs Ansicht, sodass sowohl 32-Bit-als auch 64-Bit-Anwendungen die 32-Bit-Version von Winword.exe für doc-Dateien starten.
-   Ein Administrator installiert 64-Bit-Office, das 64-Bit-Winword.exe registriert, um doc-Dateien in der 64-Bit-Registrierungs Ansicht zu verarbeiten. Der Registrierungs Reflektor kopiert diese Informationen in die 32-Bit-Registrierung, sodass sowohl 32-Bit-als auch 64-Bit-Anwendungen die 64-Bit-Version von Winword.exe für doc-Dateien starten.

Aus diesem Grund werden die Datei Zuordnungs Informationen für die zuletzt installierte Anwendung beibehalten.

Es kann nützlich sein, wenn 32-Bit-und 64-Bit-Anwendungen bestimmte Registrierungsschlüssel Werte gemeinsam verwenden, die normalerweise in separate Registrierungs Sichten geschrieben werden. Beispielsweise könnte ein 32-Bit-OLE-Server, der Anforderungen von 32-Bit-und 64-Bit-Clients bedienen kann, seine 32-Bit-Registrierungsdaten für die 64-Bit-Ansicht der Systemregistrierung verfügbar machen.

Wenn eine Komponente Daten in die Systemregistrierung schreibt, analysiert WOW64 die Informationen und erstellt bei Bedarf eine Kopie der Daten in der alternativen Ansicht der Registrierung. In der Regel werden bei diesem Prozess zwei separate physische Kopien derselben Registrierungsschlüssel sowohl in der Registrierung als auch als Registrierungs Reflektion oder als Registrierungs Spiegelung bezeichnet.

Die meisten Schlüssel unter dem Klassen Stamm befinden sich in dieser Kategorie. Updates der Schlüssel werden wiedergegeben, wenn das Update abgeschlossen und das Handle für den Schlüssel geschlossen wird. In bestimmten Fällen werden Schreibvorgänge in einen Schlüssel nicht widergespiegelt, wenn der Schlüssel eine gewisse Bielle Abhängigkeit aufweist. Beispielsweise ist der 32-Bit-InprocServer32-Schlüssel für 64-Bit-Anwendungen nicht relevant, sodass der InprocServer32-Schlüssel nicht in der 64-Bit-Registrierungs Ansicht widergespiegelt wird. 64-Bit-Anwendungen können jedoch den 32-Bit-LocalServer32-Schlüssel verwenden, und die LocalServer32-Taste wird reflektiert.

Für **HKEY \_ - \_ \\ Softwareverteilungs-Software \\ Klassen \\ CLSID** und **HKEY \_ Current \_ User \\ Software \\ Classes \\ CLSID** werden nur CLSIDs reflektiert, die InprocServer32 oder InprocHandler32 nicht angeben. Nur LocalServer32 CLSIDs werden reflektiert, da Sie außerhalb des Prozesses ausgeführt werden und entweder mit 32-oder 64-Bit-Anwendungen aktiviert werden können. InprocServer32 CLSIDs werden nicht widergespiegelt, weil es nicht möglich ist, eine 32-Bit-DLL für die Ausführung in einem 64-Bit-Prozess oder eine 64-Bit-DLL für die Ausführung in einem 32-Bit-Prozess zu laden.

Für **HKEY \_ - \_ Software Klassen des lokalen Computers \\ \\ \\ AppID** und **HKEY \_ Current \_ User \\ Software \\ Classes \\ AppID** werden die Registrierungs Werte [dllersatz](../com/dllsurrogate.md) und [dllsurrogateexe]( ../com/dllsurrogateexecutable.md) nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist.

Um die Registrierungs Reflektion für einen bestimmten reflektierten Schlüssel zu deaktivieren und zu aktivieren, verwenden Sie die Funktionen [**regdisablereflectionkey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) und [**regenablereflectionkey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) . Diese Funktionen wirken sich nicht auf Schlüssel aus, die weiter oben in diesem Thema nicht in der Liste der reflektierten Schlüssel aufgeführt sind. Anwendungen sollten die Reflektion nur für die von Ihnen erstellten Registrierungsschlüssel deaktivieren und nicht versuchen, die Reflektion für die vordefinierten Schlüssel zu deaktivieren, wie z. b. **HKEY \_ local \_ Machine** oder **HKEY \_ Current \_ User**. Verwenden Sie die [**regqueryreflectionkey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) -Funktion, um zu bestimmen, ob die Schlüssel für die reflektionsliste deaktiviert wurden.

Reflektierte Schlüssel sollten nicht in transaktiven Registrierungs Vorgängen verwendet werden. Das Schreiben in reflektierte Schlüssel während einer Transaktion kann dazu führen, dass die Transaktion fehlschlägt. Weitere Informationen zu Transaktionen finden Sie unter [Kerneltransaktions-Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungs Redirector](registry-redirector.md)
</dt> <dt>

[Registrierungs Reflektion in Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md)
</dt> </dl>

 

 