---
description: Benutzer und Anwendungen mit Administratorrechten können Netzwerk-, URL-und Medien Quell Listen Informationen für Windows Installer Anwendungen und Patches auf dem System abrufen und ändern.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Verwalten von Installations Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352325"
---
# <a name="managing-installation-sources"></a>Verwalten von Installations Quellen

Benutzer und Anwendungen mit Administratorrechten können Netzwerk-, URL-und Medien Quell Listen Informationen für Windows Installer Anwendungen und Patches auf dem System abrufen und ändern.

**Windows Installer 2,0:** Nicht unterstützt. Administratoren können Einträge in der Quell Liste nicht lesen, neu anordnen oder ersetzen und keine Quell Listen Eigenschaften ändern oder abrufen. Es ist möglich, Netzwerk Quellen, aber keine URL-oder Medienquellen zu verwalten. Administratoren können nur Quell Listen für Computer spezifische Anwendungen oder Anwendungen verwalten, die für den aktuellen Benutzer pro Benutzer installiert sind. Dadurch wird verhindert, dass Administratoren, die frühere Versionen als Windows Installer Version 3,0 verwenden, die Quell Listen Informationen für alle Benutzer im System verwalten.

**Windows Installer 3,0 und höher:** Benutzer und Anwendungen, die über Administratorrechte verfügen, können Quell Listen Informationen für Windows Installer Anwendungen und Patches, die auf dem System installiert sind, für alle Benutzer abrufen und ändern. Die Quell Listen Funktionen können zum Verwalten von Quell Listen und Quell Listen Eigenschaften für Netzwerk-, URL-und Medienquellen verwendet werden. Das Installationsprogramm kann Quell Listen von einem externen Prozess neu anordnen.

Benutzer und Anwendungen, die über Administratorrechte verfügen, können die folgenden Typen von Quell Listen Informationen lesen und ändern:

-   Quell Listen für Anwendungen und Patches, die für alle Benutzer des Systems installiert sind.
-   Quell Listen für patchquellen, die sich von den Anwendungs Quellen unterscheiden.
-   Quell Listen für URL-und Medienquellen, die neben den Netzwerk Quellen vorhanden sind.
-   Quell Listen Eigenschaften wie " [**mediapackagepath**](mediapackagepath.md)", " [**diskprompt**](diskprompt.md)", " **LastUsedSource**", " **lastusedtype**" und " **PackageName**".

Die Quell Listen Funktionen können den Bereich der gefundenen Quell Listen einschränken, indem Sie den Installations Kontext und den Benutzer Kontext angeben. Es gibt drei mögliche Installations Kontexte: pro Benutzer (nicht verwaltet), pro Computer und pro Benutzer verwaltet. Der Benutzer Kontext kann ein bestimmter Benutzer oder alle Benutzer des Systems sein.

Nicht-Administratoren können die Quell Liste einer Instanz einer Anwendung oder eines Patches nicht ändern, die unter einem Benutzer bezogenen (verwalteten oder nicht verwalteten) Kontext eines anderen Benutzers vorhanden ist. Nicht-Administratoren können die Quell Listen einer Instanz einer Anwendung oder eines Patches, die in den folgenden Kontexten installiert ist, ändern:

-   Ihr eigener Kontext pro Benutzer (nicht verwaltet).
-   Der Computer Kontext, aber nur, wenn die Richtlinien " [disablebrowse](disablebrowse.md)", " [AllowLockdownBrowse](allowlockdownbrowse.md)" und " [alwaysinstallerhöhten](alwaysinstallelevated.md) " eine Anwendung oder eine patchquelle durchsuchen können.
-   Ihr eigener, von Benutzern verwalteter Kontext, aber nur, wenn die Richtlinien " [disablebrowse](disablebrowse.md)", " [AllowLockdownBrowse](allowlockdownbrowse.md)" und " [alwaysinstallerhöhten](alwaysinstallelevated.md) " eine Anwendung oder eine patchquelle durchsuchen können.

Administratoren können jede Quell Liste ändern, die von einem nicht--Administrator geändert werden kann. Außerdem können Administratoren und Anwendungen, die über Administratorrechte verfügen, die Quell Listen einer Anwendung oder eines Patches ändern, die in den folgenden Kontexten installiert sind:

-   Pro-Computer-Kontext.
-   Ihrer eigenen, pro Benutzer (nicht verwaltet) oder eigenen, pro Benutzer verwalteten Kontext.
-   Der benutzerspezifische verwaltete Kontext eines anderen Benutzers.

> [!Note]  
> Benutzer und Anwendungen, die über Administratorrechte verfügen, können die Quell Liste einer Instanz einer Anwendung oder eines Patches, die im benutzerspezifischen Kontext eines anderen Benutzers installiert ist, nicht ändern.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Verwalten von Netzwerk-und URL-Quellen für Produkte und Patches

Verwenden Sie die [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion, um die Quell Liste der Netzwerk-und URL-Quellen für einen Patch oder eine Anwendung in einem bestimmten Kontext hinzuzufügen oder neu anzuordnen. Verwenden Sie den *dwcontext* -Parameter, um den Installations Kontext anzugeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext anzugeben.

Verwenden Sie die [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion, um eine Quell Liste für einen Patch zu erstellen, der noch nicht auf eine Anwendung im angegebenen Kontext angewendet wurde. Dies kann hilfreich sein, wenn Sie einen Patch für erweiterte Berechtigungen registrieren. Weitere Informationen zum Registrieren erhöhter Berechtigungen für einen Patch finden Sie unter [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).

Verwenden Sie die [**msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) -Funktion, um eine vorhandene Quelle für eine Anwendung oder einen Patch in einem angegebenen Kontext zu entfernen. Wenn Sie die aktuelle Quelle für eine Anwendung oder einen Patch entfernen, wird das Installationsprogramm gezwungen, die Quell Liste nach einer Quelle zu durchsuchen, wenn eine Quelle das nächste Mal benötigt wird.

Verwenden Sie die [**msisourcelistenumsources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) -Funktion, um Quellen in der Quell Liste eines angegebenen Patches oder einer Anwendung aufzulisten.

## <a name="managing-media-sources-for-products-and-patches"></a>Verwalten von Medienquellen für Produkte und Patches

Verwenden Sie die [**msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) -Funktion, um die Datenträger Informationen der Medienquelle einer registrierten Anwendung oder eines Patches hinzuzufügen oder zu aktualisieren. Jeder Eintrag wird durch eine Datenträger-ID eindeutig identifiziert. Wenn der Datenträger bereits vorhanden ist, wird er mit der neuen Volumebezeichnung und den Werte für die Datenträger Aufforderung aktualisiert. Wenn der Datenträger nicht vorhanden ist, wird ein neuer Datenträger Eintrag mit den neuen Werten erstellt.

Verwenden Sie die [**msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) -Funktion, um einen vorhandenen registrierten Datenträger unter der Medienquelle für eine Anwendung oder einen Patch in einem bestimmten Kontext zu entfernen.

Verwenden Sie die [**msisourcelistenummediadisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) -Funktion, um eine Liste von Datenträgern aufzulisten, die unter der Medienquelle für eine Anwendung oder einen Patch registriert sind.

## <a name="retrieval-and-modification-of-source-list-information"></a>Abrufen und Ändern von Quell Listen Informationen

Verwenden Sie die Funktionen [**msisourcelistgetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) und [**msisourcelistsetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) , um Informationen zur Quell Liste für eine Anwendung oder einen Patch in einem bestimmten Kontext abzurufen oder zu ändern. Verwenden Sie den *dwcontext* -Parameter, um den Installations Kontext anzugeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext anzugeben.

Der Zugriff auf Quell Listen Eigenschaften, z. b. [**mediapackagepath**](mediapackagepath.md), [**diskprompt**](diskprompt.md), **LastUsedSource**, **lastusedtype** und **PackageName** , ist möglich.

> [!Note]  
> Die " **lastusedtype** "-Quell Listen Eigenschaft kann nur gelesen werden. Sie kann nicht direkt mit der [**msisourcelistsetinfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) -Funktion festgelegt werden.

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Löschen der kompletten Quell Liste oder Erzwingen einer Quell Auflösung

Verwenden Sie die [**msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) -Funktion, um alle vorhandenen Quellen eines bestimmten Quell Typs für die angegebene Anwendung oder patchinstanz zu entfernen. Die patchregistrierung wird auch entfernt, wenn der Patch nicht von einer Anwendung im selben Kontext installiert wird. Verwenden Sie den *dwcontext* -Parameter, um den Installations Kontext anzugeben. Verwenden Sie den *szusersid* -Parameter, um den Benutzer Kontext anzugeben.

Verwenden Sie [**msisourcelistforceresolutionex**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) , um den zuletzt verwendeten Quell Eintrag für eine Anwendung oder einen Patch im angegebenen Kontext zu löschen. Diese Funktion entfernt die Registrierung der Eigenschaft **LastUsedSource**. Diese Funktion hat keine Auswirkung auf die registrierte Quell Liste. Das Löschen der **LastUsedSource** -Registrierung zwingt den Installer, eine Quell Auflösung für die registrierten Quellen durchzuführen, wenn die Quelle das nächste Mal benötigt wird.

 

 



