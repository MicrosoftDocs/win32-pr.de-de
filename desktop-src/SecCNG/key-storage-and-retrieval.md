---
description: CNG bietet ein Modell für die Speicherung privater Schlüssel, das die Anpassung an die aktuellen und zukünftigen Anforderungen der Erstellung von Anwendungen ermöglicht, die Kryptografiefeatures wie verschlüsselung mit öffentlichem oder privatem Schlüssel verwenden, sowie die Anforderungen der Speicherung von Schlüsselmaterial.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Schlüssel Storage und Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b2100f005f0ff293e34a3f4c0a7460b7a4d4e9c2b15fbe0b3577b5e52394a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907685"
---
# <a name="key-storage-and-retrieval"></a>Schlüssel Storage und Abrufen

-   [Wichtige Storage Architektur](#key-storage-architecture)
-   [Schlüsseltypen](#key-types)
-   [Unterstützte Algorithmen](#supported-algorithms)
-   [Schlüsselverzeichnisse und Dateien](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Wichtige Storage Architektur

CNG bietet ein Modell für die Speicherung privater Schlüssel, das die Anpassung an die aktuellen und zukünftigen Anforderungen der Erstellung von Anwendungen ermöglicht, die Kryptografiefeatures wie verschlüsselung mit öffentlichem oder privatem Schlüssel verwenden, sowie die Anforderungen der Speicherung von Schlüsselmaterial. Der Schlüsselspeicherrouter ist die zentrale Routine in diesem Modell und wird in Ncrypt.dll. Eine Anwendung greifen über den Schlüsselspeicherrouter auf die Schlüsselspeicheranbieter (Key Storage Providers, KSPs) im System zu, wodurch Details, z. B. die Schlüsselisolation, sowohl von der Anwendung als auch vom Speicheranbieter selbst verdeckt werden. Die folgende Abbildung zeigt den Entwurf und die Funktion der CNG-Schlüsselisolationsarchitektur.

![CNG-Schlüsselspeicheranbieter](images/cng-key-storage-provider.png)

Um allgemeine Kriterien (Common Criteria, CC) zu erfüllen, müssen die langlebigen Schlüssel isoliert werden, damit sie nie im Anwendungsprozess vorhanden sind. CNG unterstützt derzeit die Speicherung asymmetrischer privater Schlüssel mithilfe des Microsoft-Software-KSP, der in Windows Server 2008 und Windows Vista enthalten ist und standardmäßig installiert ist.

Die Schlüsselisolation ist standardmäßig in Windows Server 2008 und Windows Vista aktiviert. Das Schlüsselisolationsfeature ist auf Plattformen vor diesen nicht verfügbar. Darüber hinaus werden KSPs von Drittanbietern nicht in den Schlüsselisolationsdienst (LSA-Prozess) geladen. Nur der Microsoft KSP wird in den Schlüsselisolationsdienst geladen.

Der LSA-Prozess wird als Schlüsselisolationsprozess verwendet, um die Leistung zu maximieren. Der zugriff auf private Schlüssel wird über den Schlüsselspeicherrouter verläuft, der einen umfassenden Satz von Funktionen für die Verwaltung und Verwendung privater Schlüssel verfügbar macht.

CNG speichert den öffentlichen Teil des gespeicherten Schlüssels getrennt vom privaten Teil. Der öffentliche Teil eines Schlüsselpaars wird auch im Schlüsselisolationsdienst verwaltet und über einen lokalen Remoteprozeduraufruf (LRPC) aufgerufen. Der Schlüsselspeicherrouter verwendet LRPC beim Aufrufen des Schlüsselisolationsprozesses. Der zugriff auf private Schlüssel wird über den Router des privaten Schlüssels durchgeführt und von CNG überwacht.

Wie oben beschrieben, kann eine Vielzahl von Hardwarespeichergeräten unterstützt werden. In jedem Fall ist die Schnittstelle zu allen diesen Speichergeräten identisch. Sie umfasst Funktionen zum Ausführen verschiedener Vorgänge für private Schlüssel sowie Funktionen für die Schlüsselspeicherung und -verwaltung.

CNG bietet eine Reihe von APIs, die zum Erstellen, Speichern und Abrufen kryptografischer Schlüssel verwendet werden. Eine Liste dieser APIs finden Sie unter [CNG Key Storage Functions](cng-key-storage-functions.md).

## <a name="key-types"></a>Schlüsseltypen

CNG unterstützt die folgenden Schlüsseltypen:

-   Diffie-Hellman öffentlichen und privaten Schlüsseln.
-   Öffentlicher und privater Schlüssel des Digital Signature Algorithm (DSA, FIPS 186-2).
-   Öffentliche und private RSA-Schlüssel (PKCS \# 1).
-   Mehrere ältere öffentliche und private Schlüssel (CryptoAPI).
-   Kryptografie für elliptische Kurven: öffentliche und private Schlüssel.

## <a name="supported-algorithms"></a>Unterstützte Algorithmen

CNG unterstützt die folgenden Schlüsselalgorithmen.

| Algorithmus | Schlüssel-/Hashlänge (Bits)             |
|-----------|------------------------------------|
| RSA       | 512 bis 16384 in 64-Bit-Schritten |
| DH        | 512 bis 16384 in 64-Bit-Schritten |
| DSA       | 512 bis 1024 in 64-Bit-Schritten  |
| ECDSA     | P-256, P-384, P-521 (NIST-Kurven)  |
| ECDH      | P-256, P-384, P-521 (NIST-Kurven)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Schlüsselverzeichnisse und Dateien

Die älteren CryptoAPI-CSPs von Microsoft speichern private Schlüssel in den folgenden Verzeichnissen.

| Schlüsseltyp                | Verzeichnisse                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Benutzer privat            | %APPDATA% \\ Microsoft \\ Crypto \\ \\ *RSA-Benutzer-SID*\\<br/>%APPDATA% \\ Microsoft \\ Crypto \\ DSS-Benutzer-SID \\ \\<br/>                                                   |
| Privates lokales System    | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto RSA \\ \\ \\ S-1-5-18\\<br/>%ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ DSS \\ S-1-5-18\\<br/>   |
| Privater lokaler Dienst   | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto RSA \\ \\ \\ S-1-5-19\\<br/>%ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ DSS \\ S-1-5-19\\<br/>   |
| Privater Netzwerkdienst | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto RSA \\ \\ \\ S-1-5-20\\<br/>%ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ DSS \\ S-1-5-20\\<br/>   |
| Shared private          | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ RSA \\ \\ MachineKeys<br/>%ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ DSS \\ MachineKeys<br/> |



 

CNG speichert private Schlüssel in den folgenden Verzeichnissen.

| Schlüsseltyp                | Verzeichnis                                                          |
|-------------------------|--------------------------------------------------------------------|
| Benutzer privat            | %APPDATA% \\ Microsoft \\ Crypto \\ Keys                                 |
| Privates lokales System    | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ SystemKeys |
| Privater lokaler Dienst   | %WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Privater Netzwerkdienst | %WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Shared private          | %ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft Crypto \\ \\ Keys       |



 

Im Folgenden finden Sie einige Unterschiede zwischen den Schlüsselcontainern CryptoAPI und CNG.

-   CNG verwendet andere Dateinamen für Schlüsseldateien als Schlüsseldateien, die vom Rsaenh.dll und Dssenh.dll CSPs erstellt werden. Die älteren Schlüsseldateien haben auch die Erweiterung .key, CNG-Schlüsseldateien haben jedoch nicht die Erweiterung .key.
-   CNG unterstützt Unicode-Schlüsselcontainernamen vollständig. CNG verwendet einen Hash des Unicode-Containernamens, während CryptoAPI einen Hash des ANSI-Containernamens verwendet.
-   CNG ist in Bezug auf RSA-Schlüsselpaare flexibler. CNG unterstützt beispielsweise öffentliche Exponenten mit einer Länge von mehr als 32 Bits und Schlüssel, bei denen p und q unterschiedliche Längen haben.
-   In CryptoAPI wird die Schlüsselcontainerdatei in einem Verzeichnis gespeichert, dessen Name der Textentsprechung der SID des Benutzers entspricht. Dies ist in CNG nicht mehr der Fall, wodurch die Schwierigkeiten beim Verschieben von Benutzern aus einer Domäne in eine andere beseitigt werden, ohne dass alle privaten Schlüssel verloren geht.
-   CNG KSP und Schlüsselnamen sind auf **MAX \_ PATH Unicode-Zeichen** beschränkt. Der CryptoAPI-CSP und die Schlüsselnamen sind auf **MAX \_ PATH** ANSI-Zeichen beschränkt.
-   CNG bietet die Möglichkeit benutzerdefinierter Schlüsseleigenschaften. Benutzer können benutzerdefinierte Eigenschaften erstellen und Schlüsseln zuordnen und diese mit persistenten Schlüsseln speichern lassen.

Beim Beibehalten eines Schlüssels kann CNG zwei Dateien erstellen. Die erste Datei enthält den privaten Schlüssel im neuen CNG-Format und wird immer erstellt. Diese Datei kann von den älteren CryptoAPI-CSPs nicht verwendet werden. Die zweite Datei enthält denselben privaten Schlüssel im älteren CryptoAPI-Schlüsselcontainer. Die zweite Datei entspricht dem Format und speicherort, das von der Rsaenh.dll. Die erstellung der zweiten Datei erfolgt nur, wenn das **Flag NCRYPT \_ WRITE KEY TO LEGACY STORE \_ \_ \_ \_ \_ FLAG** angegeben wird, wenn die [**NCryptFinalizeKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) aufgerufen wird, um einen RSA-Schlüssel zu finalisieren. Dieses Feature wird für DSA- und DH-Schlüssel nicht unterstützt.

Wenn eine Anwendung versucht, einen vorhandenen persistenten Schlüssel zu öffnen, versucht CNG zunächst, die native CNG-Datei zu öffnen. Wenn diese Datei nicht vorhanden ist, versucht CNG, einen übereinstimmenden Schlüssel im älteren CryptoAPI-Schlüsselcontainer zu finden.

Wenn Sie CryptoAPI-Schlüssel von einem Quellcomputer auf einen Zielcomputer mit Windows Migrationstool für den Benutzerstatus (USMT) verschieben oder kopieren, kann CNG nicht auf die Schlüssel auf dem Zielcomputer zugreifen. Um auf solche migrierten Schlüssel zu zugreifen, müssen Sie cryptoAPI verwenden.

 

 




