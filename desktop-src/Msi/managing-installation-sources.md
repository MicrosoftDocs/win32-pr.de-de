---
description: Benutzer und Anwendungen mit Administratorrechten können Netzwerk-, URL- und Medienquelllisteninformationen für Windows Installer-Anwendungen und Patches auf dem System abrufen und ändern.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Verwalten von Installationsquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7555bc9595ba10d9ce569c15c2a8138a05348e503d86a025f0cfe1783843fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013068"
---
# <a name="managing-installation-sources"></a>Verwalten von Installationsquellen

Benutzer und Anwendungen mit Administratorrechten können Netzwerk-, URL- und Medienquelllisteninformationen für Windows Installer-Anwendungen und Patches auf dem System abrufen und ändern.

**Windows Installer 2.0:** Wird nicht unterstützt. Administratoren können keine Einträge in der Quellliste lesen, neu anordnen oder ersetzen und können keine Quelllisteneigenschaften ändern oder abrufen. Es ist möglich, Netzwerkquellen, aber keine URL- oder Medienquellen zu verwalten. Administratoren können Quelllisten nur für Computeranwendungen oder Anwendungen verwalten, die pro Benutzer für den aktuellen Benutzer installiert sind. Dadurch wird verhindert, dass Administratoren, die frühere Versionen als Windows Installer Version 3.0 verwenden, Quelllisteninformationen für alle Benutzer im System verwalten können.

**Windows Installer 3.0 und höher:** Benutzer und Anwendungen mit Administratorrechten können Quelllisteninformationen für Windows Installer-Anwendungen und -Patches, die auf dem System installiert sind, für alle Benutzer abrufen und ändern. Die Quelllistenfunktionen können zum Verwalten von Quelllisten und Quelllisteneigenschaften für Netzwerk-, URL- und Medienquellen verwendet werden. Das Installationsprogramm kann Quelllisten aus einem externen Prozess neu anordnen.

Benutzer und Anwendungen mit Administratorrechten können die folgenden Typen von Quelllisteninformationen lesen und ändern:

-   Quelllisten für Anwendungen und Patches, die für alle Benutzer auf dem System installiert sind.
-   Quelllisten für Patchquellen, die abgesehen von den Anwendungsquellen vorhanden sind.
-   Quelllisten für URL- und Medienquellen, die abgesehen von Netzwerkquellen vorhanden sind.
-   Quelllisteneigenschaften wie [**MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource,** **LastUsedType** und **PackageName**.

Die Quelllistenfunktionen können den Bereich der gefundenen Quelllisten einschränken, indem sie den Installationskontext und den Benutzerkontext angeben. Es gibt drei mögliche Installationskontexte: pro Benutzer (nicht verwaltet), pro Computer und pro Benutzer verwaltet. Der Benutzerkontext kann ein bestimmter Benutzer oder alle Benutzer im System sein.

Nichtadministratoren können die Quellliste einer Instanz einer Anwendung oder eines Patches, die im Kontext eines anderen Benutzers (verwaltet oder nicht verwaltet) vorhanden ist, nicht ändern. Nichtadministratoren können die Quelllisten einer Instanz einer Anwendung oder eines Patches ändern, die in den folgenden Kontexten installiert sind:

-   Ein eigener (nicht verwalteter) Benutzerkontext.
-   Der Computerkontext, aber nur, wenn die Richtlinien [DisableBrowse,](disablebrowse.md) [AllowLockdownBrowse](allowlockdownbrowse.md)und [AlwaysInstallElevated](alwaysinstallelevated.md) es ihnen ermöglichen, nach einer Anwendung oder Patchquelle zu suchen.
-   Ein eigener benutzerbasierter verwalteter Kontext, aber nur, wenn die Richtlinien [DisableBrowse,](disablebrowse.md) [AllowLockdownBrowse](allowlockdownbrowse.md)und [AlwaysInstallElevated](alwaysinstallelevated.md) es ihnen ermöglichen, nach einer Anwendung oder Patchquelle zu suchen.

Administratoren können jede Quellliste ändern, die ein Nichtadministrator ändern kann. Darüber hinaus können Administratoren und Anwendungen mit Administratorrechten die Quelllisten einer Anwendung oder eines Patches ändern, die in den folgenden Kontexten installiert sind:

-   Pro Computerkontext.
-   Ein eigener benutzerbasierter (nicht verwalteter) oder ein eigener benutzerbasierter verwalteter Kontext.
-   Der benutzerspezifische verwaltete Kontext eines anderen Benutzers.

> [!Note]  
> Benutzer und Anwendungen mit Administratorrechten können die Quellliste einer Instanz einer Anwendung oder eines Patches, die bzw. der im Benutzerkontext (nicht verwaltet) eines anderen Benutzers installiert ist, nicht ändern.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Verwalten von Netzwerk- und URL-Quellen für Produkte und Patches

Verwenden Sie die [**MsiSourceListAddSourceEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) um die Quellliste der Netzwerk- und URL-Quellen für einen Patch oder eine Anwendung in einem bestimmten Kontext hinzuzufügen oder neu anzuordnen. Verwenden Sie den *dwContext-Parameter,* um den Installationskontext anzugeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext anzugeben.

Verwenden Sie die [**MsiSourceListAddSourceEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) um eine Quellliste für einen Patch zu erstellen, der noch nicht auf eine Anwendung im angegebenen Kontext angewendet wurde. Dies kann nützlich sein, wenn Sie einen Patch mit erhöhten Rechten registrieren. Weitere Informationen zum Registrieren erhöhter Rechte für einen Patch finden Sie unter [Patchen Per-User Verwalteter Anwendungen.](patching-per-user-managed-applications.md)

Verwenden Sie die [**MsiSourceListClearSource-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) um eine vorhandene Quelle für eine Anwendung oder einen Patch in einem angegebenen Kontext zu entfernen. Das Entfernen der aktuellen Quelle für eine Anwendung oder einen Patch erzwingt, dass das Installationsprogramm die Quellliste nach einer Quelle durchsucht, wenn das nächste Mal eine Quelle erforderlich ist.

Verwenden Sie die [**MsiSourceListEnumSources-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) um Quellen in der Quellliste eines angegebenen Patches oder einer Anwendung aufzulisten.

## <a name="managing-media-sources-for-products-and-patches"></a>Verwalten von Medienquellen für Produkte und Patches

Verwenden Sie die [**MsiSourceListAddMediaDisk-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) um die Datenträgerinformationen der Medienquelle einer registrierten Anwendung oder eines Patches hinzuzufügen oder zu aktualisieren. Jeder Eintrag wird durch eine Datenträger-ID eindeutig identifiziert. Wenn der Datenträger bereits vorhanden ist, wird er mit der neuen Volumebezeichnung und den Eingabeaufforderungswerten des Datenträgers aktualisiert. Wenn der Datenträger nicht vorhanden ist, wird ein neuer Datenträgereintrag mit den neuen Werten erstellt.

Verwenden Sie die [**MsiSourceListClearMediaDisk-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) um einen vorhandenen registrierten Datenträger unter der Medienquelle für eine Anwendung oder einen Patch in einem bestimmten Kontext zu entfernen.

Verwenden Sie die [**MsiSourceListEnumMediaDisks-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) um eine Liste der Datenträger aufzulisten, die unter der Medienquelle für eine Anwendung oder einen Patch registriert sind.

## <a name="retrieval-and-modification-of-source-list-information"></a>Abrufen und Ändern von Quelllisteninformationen

Verwenden Sie die Funktionen [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) und [**MsiSourceListSetInfo,**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) um Informationen zur Quellliste für eine Anwendung oder einen Patch in einem bestimmten Kontext abzurufen oder zu ändern. Verwenden Sie den *dwContext-Parameter,* um den Installationskontext anzugeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext anzugeben.

Auf Quelllisteneigenschaften wie [**MEDIAPACKAGEPATH,**](mediapackagepath.md) [**DiskPrompt,**](diskprompt.md) **LastUsedSource,** **LastUsedType** und **PackageName** kann zugegriffen werden.

> [!Note]  
> Die **LastUsedType-Quelllisteneigenschaft** kann nur gelesen werden. Sie kann nicht direkt mithilfe der [**MsiSourceListSetInfo-Funktion**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) festgelegt werden.

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Löschen der vollständigen Quellliste oder Erzwingen einer Quellauflösung

Verwenden Sie die [**MsiSourceListClearAllEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) um alle vorhandenen Quellen eines bestimmten Quelltyps für die angegebene Anwendung oder Patchinstanz zu entfernen. Die Patchregistrierung wird auch entfernt, wenn der Patch nicht von einer Anwendung im gleichen Kontext installiert wird. Verwenden Sie den *dwContext-Parameter,* um den Installationskontext anzugeben. Verwenden Sie den *szUserSid-Parameter,* um den Benutzerkontext anzugeben.

Verwenden Sie [**MsiSourceListForceResolutionEx,**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) um den zuletzt verwendeten Quelleintrag für eine Anwendung oder einen Patch im angegebenen Kontext zu löschen. Diese Funktion entfernt die Registrierung der Eigenschaft **lastUsedSource**. Diese Funktion wirkt sich nicht auf die Liste der registrierten Quellen aus. Das Löschen der **LastUsedSource-Registrierung erzwingt,** dass das Installationsprogramm eine Quellauflösung für die registrierten Quellen vorgibt, wenn die Quelle das nächste Mal benötigt wird.

 

 



