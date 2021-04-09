---
title: Benutzerkontensteuerung und Bits
description: Wenn sich ein Administrator Benutzer auf dem Computer anmeldet, werden zwei Zugriffs Token erstellt. Eine ist ein gefiltertes Standardbenutzer Zugriffs Token, das andere ein vollständiges Administrator Zugriffs Token.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 3017b3a0d816ba393d1427c5c1d2315a68b2dcc0
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "103948513"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Bits-Sicherheit,-Token und-Administrator Konten

## <a name="http-server-certificate-callbacks"></a>HTTP-Server-Zertifikat Rückrufe
Das korrekte Validieren von Server Zertifikaten ist ein wichtiger Bestandteil der Verwaltung der HTTPS-Sicherheit. Bits hilft bei der stets Validierung von Server Zertifikaten anhand einer Liste von Anforderungen, die von [**setsecurityflags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags)angegeben werden. Standardmäßig verwendet Bits die Überprüfung des "Browser"-Stil Zertifikats.

Sie können auch eine benutzerdefinierte Funktion angeben, die aufgerufen werden soll, um das Zertifikat weiter zu validieren. Legen Sie den Serverzertifikat Rückruf mit der [**setservercertificatevalidationinterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) -Methode fest. Die-Methode wird nur aufgerufen, nachdem das Betriebssystem das Zertifikat auf der Grundlage des Aufrufs von [ **setsecurityflag** s](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) überprüft hat. 

## <a name="http-client-certificates"></a>HTTP-Client Zertifikate
Sie können ein Client Zertifikat für einen HTTP-Auftrag mit zwei verschiedenen Methoden für Zertifikat Einstellungen festlegen. Sie können ein Zertifikat entweder über die [ID](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) oder den [Namen](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)des Zertifikat Antragstellers festlegen. Das Client Zertifikat wird während der TLS-Aushandlung (oder der Aushandlung) verwendet, wenn für den Server eine Client Authentifizierung erforderlich ist.

## <a name="write-only-http-headers"></a>Schreibgeschützte HTTP-Header
Mit Bits können Sie http-Authentifizierungs Token vor unerwünschtem Zugriff schützen. Ein HTTP-Server benötigt häufig ein Sicherheits Token oder eine beliebige Zeichenfolge, wenn eine Datei auf http-Server heruntergeladen oder hochgeladen wird.

Bits schützt diese Authentifizierungs Token auf verschiedene Weise.
* Mithilfe von Bits können Sie TLS-und SSL-geschützte http-Verbindungen verwenden, indem Sie eine HTTPS-URL angeben.
* Benutzerdefinierte Header werden immer in einem verschlüsselten Format auf dem Datenträger gespeichert.
* Sie können verhindern, dass Kunden Header mit der [**IBackgroundCopyJobHttpOptions3:: makecustomheadersschreiteonly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) -Methode an andere Programme zurückgegeben werden.


## <a name="standard-and-administrator-users"></a>Standard-und Administrator Benutzer
Ein Benutzer, der der Administrator Gruppe angehört, kann einen Prozess mit Standardbenutzer Zugriff oder mit erhöhten Rechten (mit Administratorrechten) ausführen. Bits führt den Auftrag in einem der beiden Zustände aus, solange der Benutzer am Computer angemeldet ist. Wenn der Benutzer den Auftrag jedoch erstellt oder den Besitz des Auftrags im Zustand "erhöht" übernehmen würde, muss der Benutzer den Status "erhöht" aufweisen, um den Auftrag abzurufen oder zu ändern (andernfalls schlägt der-Befehl fehl, wenn der Zugriff verweigert wird (0x80070005)). Um den erhöhten Status eines Auftrags zu ermitteln, müssen Sie die [**IBackgroundCopyJob4:: getownerelevationstate**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) -Methode aufrufen.

Ein Standardbenutzer kann keine Aufträge auflisten oder ändern, die sich im Besitz anderer Benutzer befinden.

## <a name="integrity-level"></a>Integritäts Stufe
Zusätzlich zum Status erhöht kann die Integritäts Stufe des Tokens ermitteln, ob der Benutzer einen Auftrag ändern kann. Ein Client kann keine Aufträge ändern, die von einem Token mit einer höheren Integritäts Ebene erstellt wurden. Insbesondere verfügen viele Token des lokalen Systems über eine Integritäts Stufe, die höher als die Integritäts Stufe eines erweiterten Fensters ist, sodass Sie nicht von einem Administrator von einem normalen Befehlsfenster mit erhöhten Rechten geändert werden können. Beispielsweise werden Windows Update-und SMS-Aufträge als "LocalSystem" ausgeführt, das eine höhere Integritäts Stufe aufweist als ein Token mit erhöhten Rechten, sodass ein Administrator diese Aufträge nicht ändern oder löschen kann. Erstellen Sie einen Taskplaner Task, der als lokales System ausgeführt wird, um diesen Auftrag zu ändern. Der Task kann eine Konsolenanwendung ausführen, die die Bits-API verwendet, oder der Task kann ein Skript ausführen, das BitsAdmin.exe aufruft. Um die verwendete Integritäts Stufe zu ermitteln, müssen Sie die [**IBackgroundCopyJob4:: getownerintegratylevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) -Methode aufrufen.

## <a name="service-identity"></a>Dienst Identität
Beginnend mit dem Windows 10-Update von Mai 2019 (10,0; Build 18362), von einem Dienst gestartete BITS-Aufträge behalten die Dienst Identität bei. Dies ermöglicht es Diensten, die Bits verwenden möchten, um Dateien herunterzuladen oder Dateien aus einem Verzeichnis hochzuladen, dessen Berechtigungen an die Dienst-SID gebunden sind. Außerdem wird der Netzwerk Datenverkehr dem Dienst, der den BITS-Auftrag angefordert hat, ordnungsgemäß zugeordnet, anstatt Bits zugeordnet zu werden.

 




