---
description: CNG bietet ein Modell für den privaten Schlüsselspeicher, das die Anpassung an den aktuellen und den zukünftigen Bedarf an der Erstellung von Anwendungen ermöglicht, die Kryptografiefunktionen wie die Verschlüsselung mit öffentlichem oder öffentlichem Schlüssel verwenden, sowie die Anforderungen der Speicherung von Schlüsselmaterial.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Schlüssel Speicherung und-Abruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347758"
---
# <a name="key-storage-and-retrieval"></a>Schlüssel Speicherung und-Abruf

-   [Key Storage-Architektur](#key-storage-architecture)
-   [Schlüsseltypen](#key-types)
-   [Unterstützte Algorithmen](#supported-algorithms)
-   [Schlüssel Verzeichnisse und-Dateien](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Key Storage-Architektur

CNG bietet ein Modell für den privaten Schlüsselspeicher, das die Anpassung an den aktuellen und den zukünftigen Bedarf an der Erstellung von Anwendungen ermöglicht, die Kryptografiefunktionen wie die Verschlüsselung mit öffentlichem oder öffentlichem Schlüssel verwenden, sowie die Anforderungen der Speicherung von Schlüsselmaterial. Der Schlüsselspeicher Router ist die zentrale Routine in diesem Modell und wird in Ncrypt.dll implementiert. Eine Anwendung greift auf die Schlüsselspeicher Anbieter (Key Storage Providers, kSPS) im System über den Schlüsselspeicher Router zu, der Details, wie z. b. die Schlüssel Isolation, sowohl von der Anwendung als auch vom Speicher Anbieter selbst verbirgt. Die folgende Abbildung zeigt den Entwurf und die Funktion der Architektur der CNG-Schlüssel Isolation.

![CNG-Schlüsselspeicher Anbieter](images/cng-key-storage-provider.png)

Um die Anforderungen an die Common Criteria (CC) einzuhalten, müssen die langlebige Schlüssel isoliert werden, damit Sie im Anwendungsprozess nie vorhanden sind. CNG unterstützt derzeit die Speicherung von asymmetrischen privaten Schlüsseln mithilfe der Microsoft-Software-KSP, die in Windows Server 2008 und Windows Vista enthalten und standardmäßig installiert ist.

Die Schlüssel Isolation ist in Windows Server 2008 und Windows Vista standardmäßig aktiviert. Die Schlüssel Isolations Funktion ist auf Plattformen vor diesen nicht verfügbar. Außerdem werden Drittanbieter-kSPS nicht in den Key Isolation Service (LSA-Prozess) geladen. Nur der Microsoft KSP wird in den Schlüssel Isolations Dienst geladen.

Der LSA-Prozess wird als Schlüssel Isolations Prozess verwendet, um die Leistung zu maximieren. Der gesamte Zugriff auf private Schlüssel durchläuft den Schlüsselspeicher Router, der einen umfassenden Satz von Funktionen für die Verwaltung und Verwendung privater Schlüssel verfügbar macht.

CNG speichert den öffentlichen Teil des gespeicherten Schlüssels getrennt vom privaten Teil. Der öffentliche Teil eines Schlüssel Paars wird ebenfalls im Schlüssel Isolations Dienst verwaltet, und der Zugriff erfolgt über den lokalen Remote Prozedur Aufruf (Remote Procedure Aufruf, LRPC). Der Schlüsselspeicher Router verwendet LRPC, wenn der Schlüssel Isolations Prozess aufgerufen wird. Der gesamte Zugriff auf private Schlüssel erfolgt über den Router des privaten Schlüssels und wird von CNG überwacht.

Wie oben beschrieben, kann eine große Bandbreite an Hardware Speichergeräten unterstützt werden. In jedem Fall ist die Schnittstelle zu all diesen Speichergeräten identisch. Sie enthält Funktionen zum Durchführen verschiedener Vorgänge für private Schlüssel sowie Funktionen, die die Schlüssel Speicherung und-Verwaltung betreffen.

CNG bietet eine Reihe von APIs, die zum Erstellen, speichern und Abrufen von Kryptografieschlüsseln verwendet werden. Eine Liste dieser APIs finden Sie unter [CNG-Schlüsselspeicher Funktionen](cng-key-storage-functions.md).

## <a name="key-types"></a>Schlüsseltypen

CNG unterstützt die folgenden Schlüsseltypen:

-   Diffie-Hellman öffentlichen und privaten Schlüsseln.
-   Öffentliche und private Schlüssel für den Algorithmus für digitale Signaturen (DSA, FPS 186-2).
-   \#Öffentliche und Private RSA-Schlüssel (PKCS 1).
-   Mehrere öffentliche und private Legacy Schlüssel (CryptoAPI).
-   Öffentliche und private Schlüssel für die elliptische Kurve der Kryptografie.

## <a name="supported-algorithms"></a>Unterstützte Algorithmen

CNG unterstützt die folgenden Schlüssel Algorithmen.

| Algorithmus | Schlüssel-/Hashlänge (Bits)             |
|-----------|------------------------------------|
| RSA       | 512 bis 16384, in 64-Bit-Inkrementen |
| DH        | 512 bis 16384, in 64-Bit-Inkrementen |
| DSA       | 512 bis 1024, in 64-Bit-Inkrementen  |
| ECDsa     | P-256, p-384, p-521 (NIST-Kurven)  |
| ECDH      | P-256, p-384, p-521 (NIST-Kurven)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Schlüssel Verzeichnisse und-Dateien

Die Microsoft Legacy CryptoAPI-CSPs speichern private Schlüssel in den folgenden Verzeichnissen.

| Schlüsseltyp                | Verzeichnisse                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Benutzer privat            | % APPDATA% \\ Microsoft \\ Crypto \\ RSA- \\ *Benutzer-SID*\\<br/>% APPDATA% \\ Microsoft \\ Crypto \\ DSS- \\ *Benutzer-SID*\\<br/>                                                   |
| Lokales System privat    | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-18\\<br/>   |
| Lokaler Dienst privat   | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-19\\<br/>   |
| Netzwerkdienst privat | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-20\\<br/>   |
| Freigegeben, privat          | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ DSS \\ MachineKeys<br/> |



 

CNG speichert private Schlüssel in den folgenden Verzeichnissen.

| Schlüsseltyp                | Verzeichnis                                                          |
|-------------------------|--------------------------------------------------------------------|
| Benutzer privat            | % APPDATA% \\ Microsoft \\ - \\ Kryptografieschlüssel                                 |
| Lokales System privat    | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ Crypto \\ systemkeys |
| Lokaler Dienst privat   | % Windir% \\ ServiceProfiles \\ LocalService                            |
| Netzwerkdienst privat | % Windir% \\ ServiceProfiles \\ NetworkService                          |
| Freigegeben, privat          | % ALLUSERSPROFILE% \\ Anwendungsdaten \\ Microsoft \\ - \\ Kryptografieschlüssel       |



 

Im folgenden finden Sie einige der Unterschiede zwischen den kryptoapi-und CNG-Schlüssel Containern.

-   CNG verwendet unterschiedliche Dateinamen für Schlüsseldateien als Schlüsseldateien, die vom Rsaenh.dll und Dssenh.dll Legacy-CSPs erstellt werden. Die Legacy Schlüsseldateien verfügen ebenfalls über die Erweiterung ". Key", aber CNG-Schlüsseldateien haben nicht die Erweiterung. Key.
-   CNG unterstützt vollständige Unicode-Schlüssel Container Namen; CNG verwendet einen Hash des Unicode-Container namens, während CryptoAPI einen Hash des ANSI-Container namens verwendet.
-   CNG ist in Bezug auf RSA-Schlüsselpaare flexibler. CNG unterstützt z. b. öffentliche Exponenten mit einer Länge von mehr als 32 Bit und unterstützt Schlüssel, bei denen p und q eine unterschiedliche Länge aufweisen.
-   In CryptoAPI wird die Schlüssel Containerdatei in einem Verzeichnis gespeichert, dessen Name die Text Entsprechung der SID des Benutzers ist. Dies ist nicht mehr der Fall in CNG, wodurch die Schwierigkeit entfällt, Benutzer aus einer Domäne in eine andere zu verschieben, ohne alle Ihre privaten Schlüssel zu verlieren.
-   Der CNG-KSP und die Schlüsselnamen sind auf die **maximalen \_ Pfad** -Unicode-Zeichen beschränkt. Der CryptoAPI-CSP-und der Schlüssel Name sind auf die **maximalen \_ Pfad** -ANSI-Zeichen beschränkt.
-   CNG bietet die Funktion benutzerdefinierter Schlüsseleigenschaften. Benutzer können benutzerdefinierte Eigenschaften erstellen und mit ihnen verknüpften Schlüsseln verknüpfen.

Beim Beibehalten eines Schlüssels kann CNG zwei Dateien erstellen. Die erste Datei enthält den privaten Schlüssel im neuen CNG-Format und wird immer erstellt. Diese Datei kann von den Legacy-CryptoAPI-CSPs nicht verwendet werden. Die zweite Datei enthält den gleichen privaten Schlüssel im Legacy-kryptoapi-Schlüssel Container. Die zweite Datei entspricht dem Format und dem Speicherort, die von Rsaenh.dll verwendet werden. Die zweite Datei kann nur erstellt werden, wenn der **NCrypt- \_ Flag zum Schreiben von Schreib \_ Schlüsseln in den \_ \_ Legacy \_ Speicher \_** angegeben wird, wenn die [**ncryptfinalizekey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) -Funktion aufgerufen wird, um einen RSA-Schlüssel zu finalisieren. Diese Funktion wird für DSA-und DH-Schlüssel nicht unterstützt.

Wenn eine Anwendung versucht, einen vorhandenen persistenten Schlüssel zu öffnen, versucht CNG zuerst, die native CNG-Datei zu öffnen. Wenn diese Datei nicht vorhanden ist, versucht CNG, einen übereinstimmenden Schlüssel im Legacy-kryptoapi-Schlüssel Container zu finden.

Wenn Sie kryptoapi-Schlüssel von einem Quellcomputer auf einen Zielcomputer mit dem Windows-Migrationstool für den Benutzerstatus (Anwendungsprotokoll) verschieben oder kopieren, kann CNG nicht auf die Schlüssel auf dem Zielcomputer zugreifen. Für den Zugriff auf solche migrierten Schlüssel müssen Sie die CryptoAPI verwenden.

 

 




