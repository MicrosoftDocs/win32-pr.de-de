---
title: Registrierungslektion
description: Der Registrierungs-Redirector isoliert 32-Bit- und 64-Bit-Anwendungen, indem separate logische Ansichten bestimmter Teile der Registrierung auf WOW64 zur Verfügung stellen. Die Werte einiger Registrierungsschlüssel müssen jedoch sowohl in der 32-Bit- als auch in der 64-Bit-Ansicht identisch sein.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- Registrierung reflektion 64-Bit-Windows Programmierung
- Reflektion 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9104ba6bf4d537a597a2a45bfd9034379ed1781dd893e23633c08e9e9c1149b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899040"
---
# <a name="registry-reflection"></a>Registrierungslektion

\[Die Informationen in diesem Thema gelten für Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP. Ab Windows 7 und Windows Server 2008 R2 verwendet WOW64 keine Registrierungslektion mehr, und früher reflektierte Schlüssel werden stattdessen gemeinsam genutzt. Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind.](shared-registry-keys.md)\]

Der [Registrierungs-Redirector](registry-redirector.md) isoliert 32-Bit- und 64-Bit-Anwendungen, indem separate logische Ansichten bestimmter Teile der Registrierung auf WOW64 zur Verfügung stellen. Die Werte einiger Registrierungsschlüssel müssen jedoch sowohl in der 32-Bit- als auch in der 64-Bit-Ansicht identisch sein.

Der Prozess der *Registrierungslektion* kopiert Registrierungsschlüssel und -werte zwischen zwei Registrierungssichten, um sie synchron zu halten. Jede Ansicht verfügt über eine separate physische Kopie jedes reflektierten Registrierungsschlüssels, eine für die 32-Bit-Registrierungsansicht und die andere für die 64-Bit-Registrierungsansicht.

Ein reflektierter Schlüssel wird kopiert, wenn ein Schlüssel durch Aufrufen von [**RegCloseKey geschlossen wird.**](/windows/desktop/api/winreg/nf-winreg-regclosekey) Beachten Sie, dass dies zu einer möglichen Racebedingung führt: Wenn mehr als ein Prozess den reflektierten Schlüssel ändert, bestimmt der letzte **RegCloseKey-Aufruf** den endgültigen Wert des Schlüssels.

Der Reflektor kopiert COM-Aktivierungsdaten für lokale Server zwischen den Ansichten, kopiert jedoch keine Prozessdaten, da das 32/64-in-Process-Mischen von Daten auf 64-Bit-Windows.

Reflektion ist für freigegebene Registrierungsschlüssel oder Registrierungsschlüssel, die nicht umgeleitet werden, nicht aktiviert. Beispielsweise ist die Reflektion für den **HKEY \_ LOCAL \_ \\ MACHINE-Systemschlüssel nicht** aktiviert. Eine Liste der Registrierungsschlüssel, die umgeleitet, freigegeben oder reflektiert werden, finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind.](shared-registry-keys.md)

Bei der Registrierungslektion wird eine Richtlinie "Letzter Schreiber gewinnt" verwendet, wie im folgenden Beispiel veranschaulicht:

-   Nach einer Neuinstallation von 64-Bit-Windows wird 64-Bit-Wordpad.exe für die .doc registriert. Der Reflektor kopiert die .doc-Registrierung aus der 64-Bit-Registrierungsansicht in die 32-Bit-Registrierungsansicht.
-   Ein Administrator installiert 32-Bit-Office, das 32-Bit-Winword.exe registriert, um .doc-Dateien in der 32-Bit-Registrierungsansicht zu verarbeiten. Der Registrierungsreflektor kopiert diese Informationen in die 64-Bit-Registrierungsansicht, sodass sowohl 32-Bit- als auch 64-Bit-Anwendungen die 32-Bit-Version von Winword.exe für .doc starten.
-   Ein Administrator installiert 64-Bit-Office, das 64-Bit-Winword.exe registriert, um .doc-Dateien in der 64-Bit-Registrierungsansicht zu verarbeiten. Der Registrierungsreflektor kopiert diese Informationen in die 32-Bit-Registrierung, sodass sowohl 32-Bit- als auch 64-Bit-Anwendungen die 64-Bit-Version von Winword.exe für .doc starten.

Daher werden die Dateiassozinformationen für die zuletzt installierte Anwendung beibehalten.

Es kann für 32-Bit- und 64-Bit-Anwendungen nützlich sein, bestimmte Registrierungsschlüsselwerte gemeinsam zu verwenden, die normalerweise in separate Registrierungsansichten geschrieben werden. Beispielsweise kann ein 32-Bit-OLE-Server, der Anforderungen von 32-Bit- und 64-Bit-Clients verarbeiten kann, seine 32-Bit-Registrierungsdaten für die 64-Bit-Ansicht der Systemregistrierung verfügbar machen.

Wenn eine Komponente Daten in die Systemregistrierung schreibt, analysiert WOW64 die Informationen und macht gegebenenfalls eine Kopie der Daten in der alternativen Ansicht der Registrierung. In der Regel speichert dieser Prozess zwei separate physische Kopien derselben Registrierungsschlüssel in beiden Ansichten in der Registrierung und wird als Registrierungslektion oder Registrierungsspiegelung bezeichnet.

Die meisten Schlüssel unter dem Klassenstamm befinden sich in dieser Kategorie. Aktualisierungen der Schlüssel werden nach Abschluss des Updates widergespiegelt, und das Handle für den Schlüssel wird geschlossen. In bestimmten Fällen werden Schreibvorgänge in einen Schlüssel nicht widergespiegelt, wenn der Schlüssel über eine Bitheitsabhängigkeit verfügt. Beispielsweise ist der 32-Bit-InprocServer32-Schlüssel für 64-Bit-Anwendungen nicht relevant, sodass der InprocServer32-Schlüssel nicht in der 64-Bit-Registrierungsansicht widergespiegelt wird. 64-Bit-Anwendungen können jedoch den 32-Bit-Schlüssel LocalServer32 verwenden, und der LocalServer32-Schlüssel wird widergespiegelt.

Für **die HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\ \\ CLSID** und **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ CLSID** werden nur CLSIDs widergespiegelt, die InprocServer32 oder InprocHandler32 nicht angeben. Nur LocalServer32-CLSIDs werden widergespiegelt, da sie prozesseiiert ausgeführt werden und entweder von 32- oder 64-Bit-Anwendungen aktiviert werden können. InProcServer32-CLSIDs werden nicht widergespiegelt, da es nicht möglich ist, eine 32-Bit-DLL für die Ausführung in einem 64-Bit-Prozess oder eine 64-Bit-DLL für die Ausführung in einem 32-Bit-Prozess zu laden.

Für **die HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\ \\ Appid** und **HKEY CURRENT USER Software \_ \_ Classes \\ \\ \\ Appid** werden die [Registrierungswerte DllSurrogate](../com/dllsurrogate.md) und [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) nicht widergespiegelt, wenn ihr Wert eine leere Zeichenfolge ist.

Verwenden Sie die Funktionen [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) und [**RegEnableReflectionKey,**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) um die Registrierungsreflektion für einen bestimmten reflektierten Schlüssel zu deaktivieren und zu aktivieren. Diese Funktionen wirken sich nicht auf Schlüssel aus, die nicht in der Liste der reflektierten Schlüssel weiter oben in diesem Thema enthalten sind. Anwendungen sollten die Reflektion nur für die Registrierungsschlüssel deaktivieren, die sie erstellen, und nicht versuchen, die Reflektion für die vordefinierten Schlüssel wie **HKEY \_ LOCAL \_ MACHINE** oder **HKEY \_ CURRENT USER zu \_ deaktivieren.** Um zu bestimmen, ob die Schlüssel in der Reflektionsliste deaktiviert wurden, verwenden Sie die [**RegQueryReflectionKey-Funktion.**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey)

Reflektierte Schlüssel sollten nicht in transaktiven Registrierungsvorgängen verwendet werden. Das Schreiben in reflektierte Schlüssel während einer Transaktion kann dazu führen, dass die Transaktion fehlschlägt. Weitere Informationen zu Transaktionen finden Sie unter [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsumleitung](registry-redirector.md)
</dt> <dt>

[Registrierungslektion in Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md)
</dt> </dl>

 

 