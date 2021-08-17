---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832610510eeb74b821ec690cab93fd9af74d69ca3479508b5c0707d45f491c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769990"
---
# <a name="certmgr"></a>CertMgr

Die CertMgr-Tools ersetzen DumpCert. Sie enthält neue Funktionen für die Verwaltung von [*Zertifikaten,*](../secgloss/c-gly.md) [*Zertifikatvertrauenslisten (Certificate Trust Lists,*](../secgloss/c-gly.md) CTLs) und [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation Lists, CRLs). Das Tool wird im \\ Ordner Bin des Installationspfads des Microsoft Windows Software Development Kit (SDK) installiert.

CertMgr ist als Teil des Windows SDK verfügbar, das Sie unter herunterladen <https://go.microsoft.com/fwlink/p/?linkid=84091> können.

CertMgr führt abhängig von der im Befehl angegebenen Aktion eine von vier Funktionen aus.

**CertMgr** \[ **-add** \| **-del** \| **-put** \] \[  \] Optionen \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

In der folgenden Tabelle sind die grundlegenden Aktionen des CertMgr-Tools aufgeführt.



| Aktionsflag | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine        | Zeigt Zertifikate, CRLs oder CTLs an. Ohne Aktionsflag (nur zur Anzeige) ist *SourceName* der Name des Zertifikatspeichers oder der Datei, der bzw. die die anzuzeigenden Elemente enthält. Der Speicher kann ein [*serialisierter*](../secgloss/s-gly.md) Speicher (StoreFile) oder ein Systemspeicher sein. Standardmäßig zeigt CertMgr alle Zertifikate, CTLs oder CRLs im Zertifikatspeicher oder in der Datei an. *DestinationName* wird nicht für die Anzeige verwendet.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -add        | Kopiert Zertifikate, CTLs und CRLs in einen Zertifikatspeicher. Bei Verwendung von **-add** ist *SourceName* der Quellzertifikatspeicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *DestinationName* ist der Zielzertifikatspeicher, dem die Zertifikate, CTLs und CRLs hinzugefügt werden. Der Zielspeicher wird als [*serialisierter*](../secgloss/s-gly.md) Speicher gespeichert, sofern nicht die Option **-7** verwendet wird, die den Speicher als [*PKCS*](../secgloss/p-gly.md) \# 7-Datei speichert. Beachten Sie, dass die Option **-7** nicht verwendet werden kann, wenn der Zielspeicher ein Systemspeicher ist.<br/>                                                                                                                          |
| -del        | Löscht Zertifikate, CTLs und CRLs aus einem Zertifikatspeicher. Bei Verwendung von **-del** ist *SourceName* der Quellzertifikatspeicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *DestinationName* ist der Zielzertifikatspeicher, der Kopien der verbleibenden Zertifikate, CTLs und CRLs enthält, nachdem die angegebenen Elemente gelöscht wurden. Wenn *DestinationName* nicht angegeben ist, dient *SourceName* auch als Zielspeicher (wird geändert). Der Zielspeicher wird als [*serialisierter*](../secgloss/s-gly.md) Speicher gespeichert, sofern nicht die Option **-7** verwendet wird, die den Speicher als PKCS \# 7-Datei speichert. Beachten Sie, dass die Option **-7** nicht verwendet werden kann, wenn der Zielspeicher ein Systemspeicher ist.<br/> |
| -put        | Speichert ein [*X.509-codiertes*](../secgloss/x-gly.md) Zertifikat, eine CTL oder eine Zertifikatsperrliste in einer Datei. Bei Verwendung von **-put** ist *SourceName* der Quellzertifikatspeicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *DestinationName* ist der Name einer Datei, in der ein [*X.509-codiertes*](../secgloss/x-gly.md) Zertifikat, eine CTL und eine Zertifikatsperrliste gespeichert werden. Wenn die Option **-7** verwendet wird, wird die Datei als PKCS \# 7-Datei gespeichert.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Optionen

Die folgenden Optionen gelten für alle CertMgr-Funktionen, mit Ausnahme der angegebenen.



| Option                     | Aktionsflag                                 | Beschreibung                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | none (nur anzeigen)                         | Ausführlicher Modus. Zeigt ausführliche Informationen zu Zertifikaten, CTLs und CRLs an. Standardmäßig werden kurze Informationen angezeigt.                                                                                                                       |
| **-c**                     | alle                                         | Nur Zertifikate verwenden.                                                                                                                                                                                                                             |
| **-CTL**                   | alle                                         | Verwenden Sie nur CTLs.                                                                                                                                                                                                                                     |
| **-CRL**                   | alle                                         | Verwenden Sie nur CRLs.                                                                                                                                                                                                                                     |
| **-all**                   | **-add-del**<br/> **-put**<br/> | Fügt alle Einträge des ausgewählten Typs hinzu.                                                                                                                                                                                                               |
| **-e** *encodingType*      | alle                                         | [*Zertifikatcodierungstyp*](../secgloss/e-gly.md).                                                                                                                                             |
| **-y** *storeProviderType* | alle                                         | Store Anbietertyp.                                                                                                                                                                                                                               |
| **-7**                     | **-add-del**<br/> **-put**<br/> | Speichert den Zielspeicher als PKCS \# 7-Datei.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | alle                                         | Store Öffnenflag. Dies ist der *dwFlags-Parameter,* der an [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)übergeben wird. Der Standardwert ist CERT \_ SYSTEM \_ STORE CURRENT \_ \_ USER. Nur sinnvoll, wenn **-y** festgelegt ist. Weitere Informationen finden Sie unter **CertOpenStore**.         |
| **-n** *commonNameString*  | **-add-del**<br/> **-put**<br/> | Allgemeiner Name des Zertifikats. Kann nur mit Zertifikaten verwendet werden.                                                                                                                                                                                |
| **-sha1** *sha1Hash*       | **-add-del**<br/> **-put**<br/> | SHA1-Hash des Zertifikats, der CTL oder der Zertifikatsperrliste, das kopiert, gelöscht oder gespeichert werden soll.                                                                                                                                                                         |
| **-s**                     | alle                                         | Gibt an, dass der Speicher ein Systemspeicher ist.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | alle                                         | Registrierungsspeicherort des Systemzertifikatspeichers. Sinnvoll nur, wenn **-s** festgelegt ist. Muss entweder auf *currentUser* (Registrierungsschlüssel HKEY \_ CURRENT \_ USER) oder *localMachine* (Registrierungsschlüssel HKEY LOCAL MACHINE) festgelegt \_ \_ werden. *currentUser* ist die Standardeinstellung. |
| **-?**                     | alle                                         | Zeigt alle Optionen an.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

CertMgr wird nur in Internet Explorer 4.0 oder höher unterstützt.

CertMgr kann ein oder mehrere Zertifikate, CTLs oder CRLs kopieren, löschen oder speichern. Wenn in einer dieser Kategorien mehrere Elemente vorhanden sind, hat der Benutzer drei Optionen:

-   Verwenden Sie die Option **-all,** um alle Elemente in der angegebenen Kategorie zu kopieren, zu löschen oder zu speichern.
-   Verwenden Sie die Optionen **-n** und **-sha1,** um das zu kopierende, zu löschende oder zu speichernde Element eindeutig zu identifizieren.
-   Wenn **-all** oder **-n** und **-sha1** nicht angegeben sind, fordert CertMgr den Benutzer zur Eingabe einer Liste von Elementen auf, die kopiert, gelöscht oder gespeichert werden sollen. Der Benutzer antwortet, indem er den Index des elements eingibt, das kopiert, gelöscht oder gespeichert werden soll.

Die Aktionen von CertMgr verwenden geringfügige Variationen der Syntax und Optionen. Die Syntax und die Optionen, die für eine Aktion spezifisch sind, müssen verwendet werden.

CertMgr funktioniert mit zwei Arten von Zertifikatspeichern: StoreFile und Systemspeicher. Eine StoreFile kann eine der folgenden Arten von Dateien sein:

-   Eine codierte CTL-/CRL-/Zertifikatdatei (kann Base64-codiert sein)
-   Eine PKCS \# 7-Datei
-   Ein signiertes Dokument
-   Eine serialisierte StoreFile

Es ist nicht erforderlich, den Typ der StoreFile anzugeben. CertMgr kann den StoreFile-Typ bestimmen und die entsprechenden Aktionen ausführen.

Ein Systemspeicher ist ein Zertifikatspeicher, der sich normalerweise in der Registrierung unter **currentUser** befindet. Der Benutzer kann auf einen Systemspeicher verweisen, indem er nur seinen Namen angibt. Es ist nicht erforderlich, den Typ des Zertifikatspeicheranbieters anzugeben. Je nach Typ von StoreFile oder Systemspeicher wählt CertMgr den entsprechenden Speicheranbietertyp aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von CertMgr](using-certmgr.md)
</dt> </dl>

 

 
