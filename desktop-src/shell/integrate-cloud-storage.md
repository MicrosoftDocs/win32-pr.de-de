---
description: Zeigt, wie Sie sich als Synchronisierungs Stamm Anbieter registrieren und einen cloudspeicheranbieter in die Stamm Ebene des Navigationsbereichs integrieren.
ms.assetid: BB177EDC-8C88-4540-B2F8-994C1C8BA91C
title: Integrieren eines cloudspeicheranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21fdc5abfbf9881bfe23b00a924fce989aec7c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552105"
---
# <a name="integrate-a-cloud-storage-provider"></a>Integrieren eines cloudspeicheranbieters

Wenn Sie über einen cloudspeicheranbieter verfügen, müssen Sie einige Schritte ausführen, um dem Benutzer eine konsistente und bevorzugte Benutzerfunktion bereitzustellen. Diese beiden Dinge werden als Synchronisierungs Stamm Anbieter registriert und die Anwendung in die Stamm Ebene des Navigationsbereichs integriert.

> [!IMPORTANT]
> Das Integrieren Ihres cloudspeicheranbieters wird nur ab Windows 10 unterstützt.

 

Als erstes muss als Synchronisierungs Stamm Anbieter registriert werden. Dadurch wird die Windows-Shell über Ihre Anwendung informiert, und Ihre Anwendung ist für das Synchronisieren von Dateien unter Ihrem Synchronisierungs Stamm zuständig. Dies ermöglicht anderen Anwendungen außerdem, dass Sie diese Dateien synchronisieren, damit Sie entsprechend reagieren können. Andere Anwendungen können dann mithilfe von [**storagefile. Provider**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) den [**Display Name**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) und die [**ID**](/uwp/api/Windows.Storage.StorageProvider?view=winrt-19041) der Anwendung erhalten.

Sie müssen mehrere Registrierungseinträge erstellen, um als Synchronisierungs Stamm Anbieter registriert werden zu können. Vor dem Bereitstellen der Liste der Schlüssel-Wert-Paare sollten Sie die folgenden Platzhalter durch ihre eigenen Anwendungsdaten ersetzen.

-   *\[ Speicher Anbieter- \] ID*: der Name Ihres cloudspeicheranbieters. Dieser Name sollte unabhängig von der Version der Anwendung konsistent sein. Ein Beispiel hierfür ist onedrive.
-   *\[ Windows- \] sid*: die eindeutige Windows-SID, die den Benutzer identifiziert. Wenn Ihre APP mehrere Installationen für mehrere Benutzer auf einem einzelnen Computer unterstützt, ist dieses Element erforderlich.
-   *\[ Konto- \] ID*: der Dienstanbieter Bezeichner für das aktuelle Konto dieses Benutzers. Einige Anbieter benötigen die Möglichkeit, mehrere Synchronisierungs Stämme für einen Benutzer bereitzustellen. Ein Beispiel hierfür ist ein work-und ein persönliches Konto. Mit der *Konto-ID* können Sie mehrere Konten für einen Benutzer registrieren. Wenn Ihr Anbieter mehrere Synchronisierungs Stämme pro Benutzer unterstützt, ist dieses Element erforderlich.

Diese Platzhalter werden kombiniert, um die Synchronisierungs Stamm-ID zu bilden. Sie müssen eine **!** Zeichen zwischen den einzelnen Platzhaltern beim bilden der Synchronisierungs Stamm-ID. Hier sind die Schlüssel-Wert-Paare, die erstellt werden müssen.

-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ syncrootmanager \\**-_\[ Speicher Anbieter \] -ID_*_!_* _\[ Windows- \] sid_*_!_* _\[ Konto- \] ID_*_\\ displaynameresource_* : verweist auf die Ressource, in der die Windows-Shell oder andere Anwendungen einen benutzerfreundlichen Namen für den Synchronisierungs Stamm erhalten können.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ syncrootmanager \\**-_\[ Speicher Anbieter \] -ID_*_!_* _\[ Windows- \] sid_*_!_* _\[ Konto- \] ID_*_\\ IconResource_* : verweist auf die Ressource, in der die Windows-Shell oder andere Anwendungen ein Symbol für den Synchronisierungs Stamm erhalten können.
-   **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ syncrootmanager \\**-_\[ Speicher Anbieter \] -ID_*_!_* _\[ Windows- \] sid_*_!_* _\[ Konto- \] ID_*_\\ usersyncroots \\_*_\[ Windows \] sid_ : der Speicherort auf dem Datenträger, auf dem sich der Synchronisierungs Stamm befindet.

Wenn Sie sich nicht als Synchronisierungs Stamm Anbieter registrieren, sollten Sie außerdem den Benutzern einfachen Zugriff auf die von Ihnen bereitgestellten Daten gewähren. Der Datei-Explorer-Namespace ist so konzipiert, dass er eine Methode für diesen einfachen Zugriff bereitstellt. Wenn Sie eine Namespace Erweiterung für Ihren Anbieter erstellen und in das Datei-Explorer-Fenster einbinden, können Benutzer mit der Stamm Ebene ihrer Dienste genauso interagieren, wie Sie in anderen Datei-Explorer-Elementen verwendet werden. In diesem Thema wird erläutert, wie Sie den Datei-Explorer-Namespace erweitern, damit der Anbieter auf der Stamm Ebene im Navigationsbereich angezeigt wird.

Der Navigationsbereich des Datei-Explorer-Fensters ist der Teil des Fensters, der auf der linken Seite angezeigt wird. In der folgenden Abbildung sehen Sie die Namespace Struktur für diesen Benutzer. Die Stamm Ebene im Navigationsbereich umfasst die Objekte für **onedrive**, **diesen PC** und das **Netzwerk**. Wenn Sie die folgenden Schritte ausführen, wird die Erweiterung der gleichen Ebene hinzugefügt.

![Navigationsbereich](images/navigationpane.png)

Um die Erweiterung dem Navigationsbereich hinzuzufügen, benötigen Sie Folgendes, bevor Sie die Registrierung bearbeiten:

-   Ein Dateisystem Ordner, der die Daten enthält, die dem Benutzer angezeigt werden sollen.

-   Der Name des clouddiensts, der im Navigationsbereich angezeigt wird. Dies kann auch der Name der Instanz sein, wenn Ihr Dienst mehrere Konten unterstützt.

-   Identifizierbares Symbol für Ihre Anwendung.

-   Eine CLSID für Ihre Anwendung. Eine Möglichkeit, eine CLSID für Ihre Anwendung zu generieren, besteht darin, die Uuidgen.exe zu verwenden. Weitere Informationen zu CLSID finden Sie unter [CLSID-Schlüssel](../com/clsid-key-hklm.md) .

Mit den folgenden Schritten können Sie die Registrierung ändern, um die erforderlichen Informationen in den Datei-Explorer-Namespace zu übernehmen. In den einzelnen Schritten werden drei Dinge ausgeführt.

-   Erstellen Sie Schlüssel in der Registrierung für Ihre CLSID, die Werte für den Namen und das Symbol für Ihre Erweiterung sowie andere Informationen enthält, die das Verhalten definieren.

-   Konfigurieren Sie die Erweiterung so, dass Sie in den Navigationsbereich am richtigen Speicherort und mit der richtigen Sichtbarkeit integriert wird.

-   Konfigurieren Sie die Erweiterung so, dass Sie das erwartete Verhalten für ein Element im Navigationsbereich hat.

Diese Anweisungen verwenden speziell den **reg.exe** -Befehl, Sie können jedoch ein beliebiges Registrierungs Bearbeitungs Tool Ihrer Wahl verwenden. Sie können diese Schritte sogar in ein Installationsprogramm integrieren, das die Registrierung Programm gesteuert aktualisiert.

## <a name="instructions"></a>Instructions

### <a name="step-1-add-your-clsid-and-name-your-extension"></a>Schritt 1: Hinzufügen der CLSID und benennen der Erweiterung

Fügen Sie der Registrierung unter HKEY Current User den Namen ihrer Erweiterung hinzu \_ \_ . Außerdem fügen Sie den eindeutigen Bezeichner für diese Erweiterung hinzu. Es ist möglich, mehr als eine Erweiterung pro Benutzer hinzuzufügen. in diesem Fall benötigen Sie jedoch für jede Erweiterung einen eindeutigen Namen und Bezeichner. Dieser Name und Bezeichner müssen in den restlichen Schritten einheitlich sein. In diesem Beispiel lautet der Name *mycloudstorageapp*.

> [!IMPORTANT]
> Der in diesen Schritten angegebene Bezeichner (0672a6d1-a6e0-40fe-AB16-s25badc6d9e3) wird nur als Beispiel verwendet. Sie müssen dies in Ihre eindeutige CLSID ändern.

 

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3}/ve/t reg \_ SZ/d "mycloudstorageapp"/f**

### <a name="step-2-set-the-image-for-your-icon"></a>Schritt 2: Festlegen des Bilds für das Symbol

Geben Sie den Pfad für das Symbol an, das im Navigationsbereich angezeigt werden soll. Im folgenden Beispiel verweist *1043* auf den Ressourcen Bezeichner für das Symbol in der angegebenen DLL.

> [!IMPORTANT]
> Sie müssen den Bildpfad aktualisieren. Er sollte auf einen generischen Pfad zeigen, in dem Ihre APP ein Image installiert hat.

 

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-f25badc6d9e3} \\ DefaultIcon/ve/t reg \_ Expand \_ SZ/d%% systemroot%% \\ system32 \\imageres.dll,-1043/f**

### <a name="step-3-add-your-extension-to-the-navigation-pane-and-make-it-visible"></a>Schritt 3: Fügen Sie die Erweiterung dem Navigationsbereich hinzu, und machen Sie sie sichtbar.

Wenn dieser Wert auf "0x1" festgelegt wird, wird angegeben, dass die Erweiterung fixiert werden soll. Dadurch wird sichergestellt, dass Sie Benutzern standardmäßig angezeigt wird. Die Standardkonfiguration für einen Benutzer besteht darin, dass nur angeheftete Elemente im Navigationsbereich angezeigt werden. Benutzer können diese Einstellung ändern, indem Sie mit der rechten Maustaste in den Navigationsbereich klicken und **alle Ordner anzeigen** auswählen. Wenn Sie die Erweiterung nicht anheften möchten, können Sie diesen Wert auf 0x0 festlegen. Dadurch wird die Erweiterung nicht entfernt, sondern es wird lediglich verhindert, dass Sie standardmäßig für den Benutzer angezeigt wird.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3}/v System. ispinnedtonamespacetree/t reg \_ DWORD/d 0x1/f**

### <a name="step-4-set-the-location-for-your-extension-in-the-navigation-pane"></a>Schritt 4: Festlegen des Speicher Orts für die Erweiterung im Navigationsbereich

Dies ist wichtig, um sicherzustellen, dass der Navigationsbereich eine konsistente Benutzerfunktion bereitstellt.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3}/v sortorderindex/t reg \_ DWORD/d 0x42/f**

### <a name="step-5-provide-the-dll-that-hosts-your-extension"></a>Schritt 5: Bereitstellen der dll, die die Erweiterung hostet.

Verwenden Sie die shell32.dll, um Windows-Standardordner zu emulieren. Ändern Sie dies nur, wenn Sie einen bestimmten Grund dafür haben und mit Namespace Erweiterungen vertraut sind.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-f25badc6d9e3} \\ InProcServer32/ve/t reg \_ Expand \_ SZ/d%% systemroot%% \\ system32 \\shell32.dll/f**

### <a name="step-6-define-the-instance-object"></a>Schritt 6: Definieren des Instanzobjekts

Geben Sie an, dass die Namespace Erweiterung wie andere Datei Ordnerstrukturen im Datei-Explorer funktionieren soll. Weitere Informationen zu shellinstanzobjekten finden Sie unter [Erstellen von Shellerweiterungen mit shellinstanzobjekten](/previous-versions/ms997573(v=msdn.10)).

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3} \\ instance/v CLSID/t reg \_ SZ/d {0e5aae11-a475-4c5b-ab00-c05de400274e}/f**

### <a name="step-7-provide-the-file-system-attributes-of-the-target-folder"></a>Schritt 7: Bereitstellen der Dateisystem Attribute des Ziel Ordners

Dies ist erforderlich, um sicherzustellen, dass der Datei-Explorer für Benutzer eine konsistente und erwartete Benutzerfunktion bereitstellt. Dieser Befehl legt das **Datei \_ Attribut \_ Verzeichnis** und das **Datei Attribut "schreibgeschützt \_ \_**" fest, bei denen es sich beide um [**Datei Attribut Konstanten**](../fileio/file-attribute-constants.md)handelt.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3} \\ instance \\ initpropertybag/v Attribute/t reg \_ DWORD/d 0x11/f**

### <a name="step-8-set-the-path-for-the-sync-root"></a>Schritt 8: Festlegen des Pfads für den Synchronisierungs Stamm

Legen Sie den Pfad für den Synchronisierungs Stamm fest.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3} \\ instance \\ initpropertybag/v targetfolderpath/t reg \_ Expand \_ SZ/d%% User Profile%% \\ mycloudstorageapp/f**

### <a name="step-9-set-appropriate-shell-flags"></a>Schritt 9: Festlegen geeigneter shellflags

Legen Sie einige Flags fest, die für das Anheften der Namespace Erweiterung an die Struktur des Datei-Explorers

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3} \\ ShellFolder/v foldervalueflags/t reg \_ DWORD/d 0x28/f**

### <a name="step-10-set-the-appropriate-flags-to-control-your-shell-behavior"></a>Schritt 10: Festlegen der geeigneten Flags, um das shellverhalten zu steuern

Legen Sie die entsprechenden [**sfgao**](sfgao.md) -Flags fest. Die relevanten Flags sind sfgao \_ canCopy, sfgao \_ CANLINK, sfgao \_ Storage, sfgao \_ haspropsheet, sfgao \_ storagevorgänger, sfgao \_ filesysancestor, sfgao \_ Folder, sfgao \_ File System und sfgao \_ hassubfolder.

**REG add HKCU \\ Software \\ Classes \\ CLSID \\ {0672a6d1-a6e0-40fe-AB16-s25badc6d9e3} \\ ShellFolder/v Attribute/t reg \_ DWORD/d 0xF 080004d/f**

### <a name="step-11-register-your-extension-in-the-namespace-root"></a>Schritt 11: Registrieren der Erweiterung im Namespace Stamm

Konfigurieren Sie die Namespace Erweiterung als untergeordnetes Element des Desktop Ordners.

**REG add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ Desktop \\ Namespace \\ {0672a6d1-a6e0-40fe-AB16-f 25badc6d9e3}/ve/t reg \_ SZ/d mycloudstorageapp/f**

### <a name="step-12-hide-your-extension-from-the-desktop"></a>Schritt 12: Ausblenden der Erweiterung auf dem Desktop

Es ist wichtig, dass die Erweiterung nur im Navigationsbereich des Datei-Explorers angezeigt wird. Eine Namespace Erweiterung funktioniert nicht wie eine normale Verknüpfung. Daher sollten Sie diese Methode nicht verwenden, um eine Desktop Verknüpfung zu erstellen.

**REG add HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ hidedesktopsymbolen \\ newstartpanel/v {0672a6d1-a6e0-40fe-AB16-f 25badc6d9e3}/t reg \_ DWORD/d 0x1/f**

 

 
