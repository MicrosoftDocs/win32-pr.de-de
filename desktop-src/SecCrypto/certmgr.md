---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e248aef1f726b16d8f17098cfc9642393b963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131437"
---
# <a name="certmgr"></a>CertMgr

Die certmgr-Tools ersetzen dumpcert. Es enthält neue Funktionen für die Verwaltung von [*Zertifikaten*](../secgloss/c-gly.md), [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs). Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.

Certmgr ist als Teil des Windows SDK verfügbar, das Sie von herunterladen können <https://go.microsoft.com/fwlink/p/?linkid=84091> .

Certmgr führt abhängig von der im Befehl aufgeführten Aktion eine der vier Funktionen aus.

**Certmgr** \[ **-Hinzufügen** \| **-del** \| **-Put** \] \[  \] Optionen \[ **-s** \[ **-r** *registrylocation* \] \] *SourceName* \[ **-s** \[ **-r** *registrylocation* \] \] \[ *destinationname*\]

In der folgenden Tabelle sind die grundlegenden Aktionen des Tools "CertMgr" angegeben.



| Aktionsflag | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none        | Zeigt Zertifikate, CRLs oder CTLs an. ohne Aktionsflag (nur zur Anzeige) ist *SourceName* der Name des Zertifikat Speicher oder der Datei, der die anzuzeigenden Elemente enthält. Bei dem Speicher kann es sich um einen [*serialisierten*](../secgloss/s-gly.md) Speicher (StoreFile) oder einen Systemspeicher handeln. Standardmäßig zeigt certmgr alle Zertifikate, CTLs oder CRLs im Zertifikat Speicher oder in der Datei an. *Destinationname* wird nicht für die Anzeige verwendet.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -Hinzufügen        | Kopiert Zertifikate, CTLs und CRLs in einen Zertifikat Speicher. Wenn Sie **-Add** verwenden, ist *SourceName* der Quell Zertifikat Speicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *Destinationname* ist der Ziel Zertifikat Speicher, dem die Zertifikate, CTLs und CRLs hinzugefügt werden. Der Zielspeicher wird als [*serialisierter*](../secgloss/s-gly.md) Speicher gespeichert, es sei denn, die Option " **-7** " wird verwendet, wodurch der Speicher als [*PKCS*](../secgloss/p-gly.md) \# 7-Datei gespeichert wird. Beachten Sie, dass die Option **-7** nicht verwendet werden kann, wenn der Zielspeicher ein Systemspeicher ist.<br/>                                                                                                                          |
| -del        | Löscht Zertifikate, CTLs und CRLs aus einem Zertifikat Speicher. Bei Verwendung von **-del** ist *SourceName* der Quell Zertifikat Speicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *Destinationname* ist der Ziel Zertifikat Speicher, der Kopien der verbleibenden Zertifikate, CTLs und CRLs enthält, nachdem die angegebenen Elemente gelöscht wurden. Wenn *destinationname* nicht angegeben wird, dient *SourceName* auch als Zielspeicher (wird geändert). Der Zielspeicher wird als [*serialisierter*](../secgloss/s-gly.md) Speicher gespeichert, es sei denn, die Option " **-7** " wird verwendet, wodurch der Speicher als PKCS 7-Datei gespeichert wird \# . Beachten Sie, dass die Option **-7** nicht verwendet werden kann, wenn der Zielspeicher ein Systemspeicher ist.<br/> |
| -Put        | Speichert ein [*X. 509*](../secgloss/x-gly.md) -codiertes Zertifikat, eine CTL oder eine CRL in einer Datei. Bei Verwendung von **-Put** ist *SourceName* der Quell Zertifikat Speicher, der die vorhandenen Zertifikate, CTLs und CRLs enthält. *Destinationname* ist der Name einer Datei, in der ein [*X. 509*](../secgloss/x-gly.md) -codiertes Zertifikat, eine CTL und eine CRL gespeichert werden. Wenn die Option **-7** verwendet wird, wird die Datei als PKCS \# 7-Datei gespeichert.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Optionen

Die folgenden Optionen gelten für alle certmgr-Funktionen, sofern nicht angegeben.



| Option                     | Aktionsflag                                 | BESCHREIBUNG                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | keine (nur Anzeige)                         | Ausführlicher Modus. Zeigt ausführliche Informationen zu Zertifikaten, CTLs und CRLs an. Der Standardwert besteht darin, kurze Informationen anzuzeigen.                                                                                                                       |
| **-c**                     | all                                         | Verwenden Sie nur Zertifikate.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Verwenden Sie nur CTLs.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | Verwenden Sie nur CRLs.                                                                                                                                                                                                                                     |
| **-Alle**                   | **-Add-del**<br/> **-Put**<br/> | Fügt alle Einträge des ausgewählten Typs hinzu.                                                                                                                                                                                                               |
| **-e** *EncodingType*      | all                                         | Der [*zertifikatcodierungstyp*](../secgloss/e-gly.md).                                                                                                                                             |
| **-y** *storeprovidertype* | all                                         | Speicher Anbietertyp.                                                                                                                                                                                                                               |
| **2-7**                     | **-Add-del**<br/> **-Put**<br/> | Speichert den Zielspeicher als PKCS \# 7-Datei.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Geöffnetes Flag speichern. Dies ist der an [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)übergebenen *dwFlags* -Parameter. Der Standardwert ist CERT \_ System \_ Store \_ Current \_ User. Nur sinnvoll, wenn **-y** festgelegt ist. Weitere Informationen finden Sie unter **certopendstore**.         |
| **-n** *commonnamestring*  | **-Add-del**<br/> **-Put**<br/> | Der allgemeine Name des Zertifikats. Kann nur mit Zertifikaten verwendet werden.                                                                                                                                                                                |
| **-SHA1** *sha1Hash*       | **-Add-del**<br/> **-Put**<br/> | Der SHA1-Hash des Zertifikats, der CTL oder der CRL, das kopiert, gelöscht oder gespeichert werden soll.                                                                                                                                                                         |
| **-s**                     | all                                         | Gibt an, dass der Speicher ein Systemspeicher ist.                                                                                                                                                                                                        |
| **-r** *registrylocation*  | all                                         | Der Registrierungs Speicherort des Systemzertifikat Speicher. Nur sinnvoll, wenn **-s** festgelegt ist. Muss entweder auf *CurrentUser* (Registrierungsschlüssel HKEY \_ Current \_ User) oder *LocalMachine* (Registrierungsschlüssel HKEY \_ local \_ Machine) festgelegt werden. *CurrentUser* ist die Standardeinstellung. |
| **-?**                     | all                                         | Zeigt alle Optionen an.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Certmgr wird nur in Internet Explorer 4,0 oder höher unterstützt.

Certmgr kann ein oder mehrere Zertifikate, CTLs oder CRLs kopieren, löschen oder speichern. Wenn in einer dieser Kategorien mehr als ein Element vorhanden ist, verfügt der Benutzer über drei Optionen:

-   Verwenden Sie die Option " **-all** ", um alle Elemente in der angegeben Kategorie zu kopieren, zu löschen oder zu speichern.
-   Verwenden Sie die Optionen **-n** und **-SHA1** , um das Element eindeutig zu identifizieren, das kopiert, gelöscht oder gespeichert werden soll.
-   Wenn " **-all**" oder "- **n** " und " **-SHA1** " nicht angegeben werden, wird der Benutzer von certmgr zu einer Liste von Elementen aufgefordert, die kopiert, gelöscht oder gespeichert werden sollen. Der Benutzer antwortet, indem er den Index des Elements, das kopiert, gelöscht oder gespeichert werden soll, eingeben.

Die Aktionen von certmgr verwenden leichte Variationen der Syntax und Optionen. Die für eine Aktion spezifischen Syntax und Optionen müssen verwendet werden.

Certmgr funktioniert mit zwei Arten von Zertifikat speichern: StoreFile und Systemspeicher. Eine StoreFile kann eine der folgenden Arten von Dateien sein:

-   Eine codierte CTL/CRL/Zertifikatsdatei (kann Base 64-codiert sein)
-   Eine PKCS \# 7-Datei
-   Ein signiertes Dokument
-   Eine serialisierte StoreFile

Der Typ der StoreFile muss nicht angegeben werden. Certmgr kann den Typ StoreFile ermitteln und die entsprechenden Aktionen ausführen.

Ein Systemspeicher ist ein Zertifikat Speicher, der sich normalerweise in der Registrierung unter " **CurrentUser**" befindet. Der Benutzer kann auf einen Systemspeicher verweisen, indem er nur seinen Namen bereitstellt. Es ist nicht erforderlich, den Typ des Zertifikat Speicher Anbieters anzugeben. Abhängig vom Typ der StoreFile oder des System Stores wählt certmgr den entsprechenden Speicher Anbietertyp aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von certmgr](using-certmgr.md)
</dt> </dl>

 

 
