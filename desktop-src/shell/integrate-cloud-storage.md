---
description: Zeigt, wie Sie sich als Synchronisierungsstammanbieter registrieren und einen Cloudspeicheranbieter in die Stammebene des Navigationsbereichs integrieren.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integrieren eines Cloud Storage-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e218caa292e2b85e13e00374562c172158be8bb2f062f25b47979902046282c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458200"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integrieren eines Cloud Storage-Anbieters

Wenn Sie über einen Cloudspeicheranbieter verfügen, sollten Sie einige Schritte ausführen, um eine konsistente und bevorzugte Benutzeroberfläche für den Benutzer bereitzustellen. Diese beiden Dinge registrieren sich als Synchronisierungsstammanbieter und integrieren Ihre Anwendung in die Stammebene des Navigationsbereichs.

> [!IMPORTANT]
> Die Integration Ihres Cloudspeicheranbieters wird nur ab Windows 10 unterstützt.

 

Zunächst müssen Sie sich als Synchronisierungsstammanbieter registrieren. Dies informiert Windows Shell über Ihre Anwendung und darüber, dass Ihre Anwendung für die Synchronisierung von Dateien im Synchronisierungsstamm verantwortlich ist. Dadurch werden auch andere Anwendungen darüber informieren, dass Sie diese Dateien synchronisieren, damit sie entsprechend reagieren können. Andere Anwendungen können dann [**StorageFile.Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) verwenden, um den [**DisplayName**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) und die [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) Ihrer Anwendung abzurufen.

Um sich als Synchronisierungsstammanbieter zu registrieren, müssen Sie mehrere Registrierungseinträge erstellen. Bevor Sie die Liste der Schlüssel-Wert-Paare bereitstellen, finden Sie hier einige Platzhalter, die Sie durch Ihre eigenen Anwendungsdaten ersetzen sollten.

-   *\[ Speicheranbieter-ID: \]* Der Name Ihres Cloudspeicheranbieters. Dieser Name sollte unabhängig von der Version Ihrer Anwendung konsistent sein. Ein Beispiel hierfür ist OneDrive.
-   *\[ Windows SID: \]* Die eindeutige Windows SID, die den Benutzer identifiziert. Wenn Ihre App mehrere Installationen für mehrere Benutzer auf einem einzelnen Computer unterstützt, ist dieser Teil erforderlich.
-   *\[ Konto-ID: \]* Der Dienstanbieterbezeichner für das aktuelle Konto dieses Benutzers. Einige Anbieter erfordern die Möglichkeit, mehrere Synchronisierungsstammeinstellungen für einen Benutzer bereitzustellen. Ein Beispiel hierfür sind ein Arbeitskonto und ein persönliches Konto. Mit der *Konto-ID* können Sie mehrere Konten für einen Benutzer registrieren. Wenn Ihr Anbieter mehrere Synchronisierungsstammeinstellungen pro Benutzer unterstützt, ist dieser Teil erforderlich.

Diese Platzhalter werden kombiniert, um die Stamm-ID der Synchronisierung zu bilden. Sie müssen eine **!** Zeichen zwischen den Platzhaltern, wenn die Stamm-ID der Synchronisierung gebildet wird. Hier sind die Schlüssel-Wert-Paare, die erstellt werden müssen.

-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ \\ SyncRootManager-Speicheranbieter-ID**_\[ \]_*_!_* _\[ Windows \] SID_*_!_* _\[ Konto-ID \]_*_\\ DisplayNameResource:_* Verweist auf die Ressource, in der die Windows Shell oder andere Anwendungen einen benutzerfreundlichen Namen für Ihren Synchronisierungsstamm erhalten können.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ \\ SyncRootManager-Speicheranbieter-ID**_\[ \]_*_!_* _\[ Windows \] SID_*_!_* _\[ \] Konto-ID-SymbolRessource:_ Verweist auf die Ressource, in der die Windows Shell oder andere Anwendungen ein Symbol für Ihren Synchronisierungsstamm erhalten können.*_\\_*
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ \\ SyncRootManager-Speicheranbieter-ID**_\[ \]_*_!_* _\[ Windows \] SID_*_!_* _\[ Konto-ID \]_*_\\ UserSyncRoots \\_*_\[ Windows \] SID:_ Der Speicherort auf dem Datenträger, an dem sich der Synchronisierungsstamm befindet.

Neben der Registrierung als Synchronisierungsstammanbieter sollen Benutzer auch einfachen Zugriff auf die von Ihnen zur Verfügung stellen Daten haben. Der Datei-Explorer-Namespace ist so konzipiert, dass er eine Methode für diesen einfachen Zugriff bereitstellt. Wenn Sie eine Namespaceerweiterung für Ihren Anbieter erstellen und in das Datei-Explorer-Fenster integrieren, können Benutzer mit der Stammebene Ihrer Dienste interagieren, so wie sie es mit anderen Datei-Explorer-Elementen gewohnt sind. In diesem Thema wird erläutert, wie Sie den Datei-Explorer-Namespace erweitern, sodass Ihr Anbieter auf der Stammebene im Navigationsbereich angezeigt wird.

Der Navigationsbereich des Datei-Explorer-Fensters ist der Teil des Fensters, der auf der linken Seite angezeigt wird. In der folgenden Abbildung sehen Sie die Namespacestruktur für diesen Benutzer. Die Stammebene im Navigationsbereich enthält die Objekte für **OneDrive**, **This PC** und **Network**. Wenn Sie diese Schritte ausführen, wird Ihre Erweiterung auf derselben Ebene hinzugefügt.

![Navigationsbereich](images/navigationpane.png)

Um Ihre Erweiterung dem Navigationsbereich hinzuzufügen, benötigen Sie Folgendes, bevor Sie die Registrierung bearbeiten können:

-   Ein Dateisystemordner, der die Daten enthält, die dem Benutzer angezeigt werden sollen.

-   Der Name Ihres Clouddiensts, der im Navigationsbereich angezeigt wird. Dies kann auch der Name der Instanz sein, wenn Ihr Dienst mehrere Konten unterstützt.

-   Identifizierbares Symbol für Ihre Anwendung.

-   Eine CLSID für Ihre Anwendung. Eine Möglichkeit zum Generieren einer CLSID für Ihre Anwendung ist die Verwendung des Uuidgen.exe. Weitere Informationen zu CLSID finden Sie unter [CLSID-Schlüssel.](../com/clsid-key-hklm.md)

Mit den folgenden Schritten wird die Registrierung geändert, um die erforderlichen Informationen in den Datei-Explorer-Namespace abzurufen. Die spezifischen Schritte erledigen drei Dinge.

-   Erstellen Sie Schlüssel in der Registrierung für Ihre CLSID, die Werte für den Namen und das Symbol für Ihre Erweiterung sowie andere Informationen enthält, die das Verhalten definieren.

-   Konfigurieren Sie Ihre Erweiterung so, dass sie am richtigen Ort und mit der richtigen Sichtbarkeit in den Navigationsbereich integriert wird.

-   Konfigurieren Sie Ihre Erweiterung so, dass sie das erwartete Verhalten für ein Element im Navigationsbereich aufweisen kann.

In diesen Anweisungen wird speziell der **befehlreg.exe** verwendet. Sie können jedoch ein beliebiges Tool zur Bearbeitung der Registrierung Ihrer Wahl verwenden. Sie können diese Schritte sogar in ein Installationsprogramm integrieren, das die Registrierung programmgesteuert aktualisiert.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Schritt 1: Hinzufügen Ihrer CLSID und Benennen der Erweiterung

Fügen Sie der Registrierung unter HKEY CURRENT USER den Namen Ihrer Erweiterung \_ \_ hinzu. Außerdem fügen Sie den eindeutigen Bezeichner für diese Erweiterung hinzu. Es ist möglich, mehr als eine Erweiterung pro Benutzer hinzuzufügen. In diesem Fall benötigen Sie jedoch einen eindeutigen Namen und Bezeichner für jede Erweiterung. Dieser Name und Bezeichner müssen während der restlichen Schritte konsistent sein. In diesem Beispiel lautet der Name *MyCloudStorageApp*.

> [!IMPORTANT]
> Der in diesen Schritten bereitgestellte Bezeichner (0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3) wird nur als Beispiel verwendet. Sie müssen dies in Ihre eindeutige CLSID ändern.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d "MyCloudStorageApp" /f**

### <a name="step-2-set-the-image-for-your-icon"></a>Schritt 2: Festlegen des Images für Ihr Symbol

Geben Sie den Pfad zum Symbol an, das im Navigationsbereich angezeigt werden soll. Im folgenden Beispiel bezieht sich *1043* auf den Ressourcenbezeichner für das Symbol in der angegebenen DLL.

> [!IMPORTANT]
> Sie müssen den Imagepfad aktualisieren. Sie sollte auf einen generischen Pfad verweisen, in dem Ihre App ein Image installiert hat.

 

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ DefaultIcon /ve /t REG \_ EXPAND SZ \_ /d %%SystemRoot%% \\ system32 \\imageres.dll,-1043 /f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Schritt 3: Hinzufügen der Erweiterung zum Navigationsbereich und Anzeigen der Erweiterung

Das Festlegen dieses Werts auf 0x1 gibt an, dass die Erweiterung angeheftet werden soll. Dadurch wird sichergestellt, dass sie Benutzern standardmäßig angezeigt wird. Die Standardkonfiguration für einen Benutzer ist, dass nur angeheftete Elemente im Navigationsbereich angezeigt werden. Ein Benutzer kann diese Einstellung ändern, indem er mit der rechten Maustaste im Navigationsbereich klickt und **alle Ordner anzeigen** auswählt. Wenn Sie Ihre Erweiterung nicht anheften möchten, können Sie diesen Wert auf 0x0 festlegen. Dadurch wird Ihre Erweiterung nicht entfernt, sondern lediglich verhindert, dass sie dem Benutzer standardmäßig angezeigt wird.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v System.IsPinnedToNameSpaceTree /t REG \_ DWORD /d 0x1 /f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Schritt 4: Festlegen des Speicherorts für Ihre Erweiterung im Navigationsbereich

Dies ist wichtig, um sicherzustellen, dass der Navigationsbereich eine konsistente Benutzeroberfläche für den Benutzer bereitstellt.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /v SortOrderIndex /t REG \_ DWORD /d 0x42 /f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Schritt 5: Geben Sie die DLL an, die Ihre Erweiterung hostet.

Verwenden Sie die shell32.dll, um Standardfensterordner zu emulieren. Ändern Sie dies nur, wenn Sie einen bestimmten Grund dafür haben und mit Namespaceerweiterungen vertraut sind.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ InProcServer32 /ve /t REG \_ EXPAND SZ \_ /d %%systemroot%% \\ system32 \\shell32.dll /f**

### <a name="step-6-define-the-instance-object"></a>Schritt 6: Definieren des Instanzobjekts

Geben Sie an, dass Ihre Namespaceerweiterung wie andere Dateiordnerstrukturen im Datei-Explorer funktionieren soll. Weitere Informationen zu Shellinstanzobjekten finden Sie unter [Erstellen von Shellerweiterungen mit Shellinstanzobjekten.](/previous-versions/ms997573(v=msdn.10))

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance /v CLSID /t REG \_ SZ /d {0E5AAE11-A475-4c5b-AB00-C66DE400274E} /f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Schritt 7: Bereitstellen der Dateisystemattribute des Zielordners

Dies ist erforderlich, um sicherzustellen, dass der Datei-Explorer eine konsistente und erwartete Benutzererfahrung bietet. Mit diesem Befehl werden **FILE \_ ATTRIBUTE \_ DIRECTORY** und **FILE ATTRIBUTE \_ \_ READONLY** festgelegt. Beide sind [**Dateiattributkonstanten.**](../fileio/file-attribute-constants.md)

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v Attributes /t REG \_ DWORD /d 0x11 /f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Schritt 8: Festlegen des Pfads für den Synchronisierungsstamm

Legen Sie den Pfad für den Synchronisierungsstamm fest.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ Instance \\ InitPropertyBag /v TargetFolderPath /t REG \_ EXPAND SZ \_ /d %%USERPROFILE%% \\ MyCloudStorageApp /f**

### <a name="step-9-set-appropriate-shell-flags"></a>Schritt 9: Festlegen geeigneter Shellflags

Legen Sie einige Flags fest, die erforderlich sind, um die Namespaceerweiterung an die Datei-Explorer-Struktur anzuheften.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v FolderValueFlags /t REG \_ DWORD /d 0x28 /f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Schritt 10: Festlegen der entsprechenden Flags zum Steuern des Shellverhaltens

Legen Sie die entsprechenden [**SFGAO-Flags**](sfgao.md) fest. Die relevanten Flags sind SFGAO \_ CANCOPY, SFGAO \_ CANLINK, SFGAO \_ STORAGE, SFGAO \_ HASPROPSHEET, SFGAO \_ STORAGEANCESTOR, SFGAO \_ FILESYSANCESTOR, SFGAO \_ FOLDER, SFGAO \_ FILESYSTEM und SFGAO \_ HASSUBFOLDER.

**reg add HKCU \\ Software \\ Classes \\ CLSID \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} \\ ShellFolder /v Attributes /t REG \_ DWORD /d 0xF080004D /f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Schritt 11: Registrieren der Erweiterung im Namespacestamm

Konfigurieren Sie die Namespaceerweiterung als untergeordnetes Element des Desktopordners.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer Desktop \\ \\ \\ NameSpace \\ {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /ve /t REG \_ SZ /d MyCloudStorageApp /f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Schritt 12: Ausblenden der Erweiterung auf dem Desktop

Es ist wichtig, dass Ihre Erweiterung nur im Navigationsbereich des Datei-Explorers angezeigt wird. Eine Namespaceerweiterung funktioniert nicht wie eine normale Verknüpfung. Daher sollten Sie diese Methode nicht verwenden, um eine Desktopverknüpfung zu erstellen.

**reg add HKCU \\ Software \\ Microsoft Windows \\ \\ CurrentVersion Explorer \\ \\ HideDesktopIcons \\ NewStartPanel /v {0672A6D1-A6E0-40FE-AB16-F25BADC6D9E3} /t REG \_ DWORD /d 0x1 /f**

 

 
