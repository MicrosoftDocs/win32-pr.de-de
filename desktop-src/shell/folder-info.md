---
description: Im Abschnitt "erhalten eines Ordners" mit der ID "" werden zwei Ansätze erläutert, mit denen Sie den Zeiger eines Namespace Objekts auf eine Element Bezeichner-Liste (PIDL)
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Erhalten von Informationen über den Inhalt eines Ordners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993686"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Erhalten von Informationen über den Inhalt eines Ordners

Im Abschnitt " [erhalten eines Ordners](folder-id.md) " mit der ID "" werden zwei Ansätze erläutert, mit denen Sie den Zeiger eines Namespace Objekts auf eine Element Bezeichner-Liste (PIDL) Eine offensichtliche Frage ist: Wenn Sie über eine PIDL verfügen, was können Sie damit tun? Eine verwandte Frage ist: Was geschieht, wenn keiner der Ansätze funktioniert oder für Ihre Anwendung geeignet ist? Die Antwort auf beide Fragen erfordert einen genaueren Blick darauf, wie der Namespace implementiert wird. Der Schlüssel ist die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle.

-   [Verwenden der IShellFolder-Schnittstelle](#using-the-ishellfolder-interface)
-   [Auflisten des Inhalts eines Ordners](#enumerating-the-contents-of-a-folder)
-   [Bestimmen von anzeigen Amen und anderen Eigenschaften](#determining-display-names-and-other-properties)
-   [Ein Zeiger auf die IShellFolder-Schnittstelle eines unter Ordners wird erhalten.](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Bestimmen des übergeordneten Ordners eines Objekts](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Verwenden der IShellFolder-Schnittstelle

An früherer Stelle in dieser Dokumentation wurden Namespace Ordner als Objekte bezeichnet. Obwohl der Begriff zu diesem Zeitpunkt in einem lockeren Sinn verwendet wurde, ist er auch in einem strengen Sinn. Jeder Namespace Ordner wird durch ein Component Object Model (com)-Objekt dargestellt. Jedes Ordner Objekt stellt eine Reihe von Schnittstellen zur Verfügung, die für eine Vielzahl von Aufgaben verwendet werden können. Einige optionale Schnittstellen werden möglicherweise nicht von allen Ordnern verfügbar gemacht. Alle Ordner müssen jedoch die grundlegende Schnittstelle ( [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)) verfügbar machen.

Der erste Schritt bei der Verwendung eines Ordner Objekts besteht darin, einen Zeiger auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle abzurufen. Zusätzlich zur Bereitstellung des Zugriffs auf die anderen Schnittstellen des Objekts macht **IShellFolder** eine Gruppe von Methoden verfügbar, die eine Reihe allgemeiner Aufgaben verarbeiten, von denen einige in diesem Abschnitt erläutert werden.

Zum Abrufen eines Zeigers auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle eines Namespace Objekts müssen Sie zuerst [**shgetdesktopfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder)aufrufen. Diese Funktion gibt einen Zeiger auf die **IShellFolder** -Schnittstelle des Namespace Stamms, den Desktop, zurück. Wenn Sie über die **IShellFolder** -Schnittstelle des Desktops verfügen, gibt es eine Vielzahl von Möglichkeiten, um fortzufahren.

Wenn Sie bereits über die PIDL des Ordners verfügen, an dem Sie interessiert sind – beispielsweise durch Aufrufen von [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)– können Sie die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle abrufen, indem Sie die [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) -Methode des Desktops aufrufen. Wenn Sie über den Pfad eines Dateisystem Objekts verfügen, müssen Sie zuerst seine PIDL abrufen, indem Sie die [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) -Methode des Desktops aufrufen und dann **IShellFolder:: BindToObject** aufrufen. Wenn keiner dieser Ansätze zutrifft, können Sie andere **IShellFolder** -Methoden verwenden, um durch den Namespace zu navigieren. Weitere Informationen finden Sie unter [Navigieren im-Namespace](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Auflisten des Inhalts eines Ordners

Der erste Schritt, den Sie in der Regel mit einem Ordner durchführen möchten, besteht darin, herauszufinden, was darin enthalten ist. Sie müssen zuerst die [**IShellFolder:: erumujects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) -Methode des Ordners aufzurufen. Im Ordner wird ein Standardmäßiges OLE-Enumerationsobjekt erstellt und dessen [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Schnittstelle zurückgegeben. Diese Schnittstelle stellt vier Standardmethoden –[**Clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)und [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)– zur Verfügung, mit denen der Inhalt des Ordners aufgelistet werden kann.

Das grundlegende Verfahren zum Auflisten des Inhalts eines Ordners lautet:

1.  Rufen Sie die Ordner [**IShellFolder:: enumubjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) -Methode auf, um einen Zeiger auf die [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Schnittstelle eines Enumerationsobjekts abzurufen.
2.  Übergeben Sie eine nicht zugeordnete PIDL an [**ienumittellist:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Im **nächsten** Schritt wird die Zuweisung der PIDL übernommen, aber die Anwendung muss die Zuordnung aufheben, wenn Sie nicht mehr benötigt wird. Wenn **Next** zurückgibt, enthält die PIDL nur die Element-ID des Objekts und die abschließenden **null** Zeichen. Das heißt, es handelt sich um eine PIDL auf einer Ebene, die relativ zum Ordner ist, nicht um eine voll qualifizierte PIDL.
3.  Wiederholen Sie Schritt 2, bis [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) den Wert false zurückgibt, \_ um anzugeben, dass alle Elemente aufgezählt wurden.
4.  Ruft **ienumittellist:: Release** auf, um das Enumerationsobjekt freizugeben.

> [!Note]  
> Es ist wichtig, zu verfolgen, ob Sie mit einer vollständigen oder relativen PIDL arbeiten. Einige Funktionen und Methoden akzeptieren beides, aber andere nehmen nur eine oder die andere auf.

 

Die verbleibenden drei [**ienumittellist**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) -Methoden ([**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)und [**Clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) sind hilfreich, wenn Sie wiederholte Enumerationen des Ordners ausführen müssen. Sie ermöglichen es Ihnen, die Enumeration zurückzusetzen, ein oder mehrere Objekte zu überspringen und eine Kopie des Enumerationsobjekt zu erstellen, um seinen Zustand beizubehalten.

## <a name="determining-display-names-and-other-properties"></a>Bestimmen von anzeigen Amen und anderen Eigenschaften

Nachdem Sie alle pidls aufgezählt haben, die in einem Ordner enthalten sind, können Sie herausfinden, welche Art von Objekten Sie darstellen. Die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle bietet eine Reihe nützlicher Methoden, von denen zwei hier erläutert werden. Andere **IShellFolder** -Methoden und andere shellordnerschnittstellen werden später erläutert.

Eine der nützlichsten Eigenschaften ist der Anzeige Name des Objekts. Um den anzeigen Amen eines Objekts abzurufen, übergeben Sie seine PIDL an [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Obwohl das-Objekt sich an einer beliebigen Stelle unterhalb des übergeordneten Ordners im-Namespace befinden kann, muss seine PIDL relativ zum Ordner sein.

[**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) gibt den anzeigen Amen als Teil einer " [**Strauch**](/windows/desktop/api/Shtypes/ns-shtypes-strret) Struktur" zurück. Da das Extrahieren des anzeigen Amens aus einer " **strinret** "-Struktur etwas kompliziert sein kann, bietet die Shell zwei Funktionen, die den Auftrag für Sie ausführen: " [**strauretystr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) " und " [**Strauch**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)". Beide Funktionen nehmen eine " **strinret** "-Struktur an und geben den anzeigen Amen als normale Zeichenfolge zurück. Sie unterscheiden sich nur in der Zuordnung der Zeichenfolge.

Neben dem anzeigen Amen kann ein Objekt über eine Reihe von Attributen verfügen, z. b. ob es sich um einen Ordner handelt oder ob es verschoben werden kann. Sie können die Attribute eines Objekts abrufen, indem Sie die zugehörige PIDL an [**IShellFolder:: getattributesof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)übergeben. Die komplette Liste der Attribute ist recht groß. Daher sollte der Verweis auf Details angezeigt werden. Beachten Sie, dass die PIDL, die Sie an **getattributesof** übergeben, eine einzelne Ebene aufweisen muss. **IShellFolder:: getattributesof** akzeptiert insbesondere die pidls, die von [**ienumittellist:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next)zurückgegeben werden. Sie können ein Array von pidls übergeben, und **getattributesof** gibt die Attribute zurück, die alle Objekte im Array gemeinsam haben.

Wenn Sie über den voll qualifizierten Pfad oder PIDL eines Objekts verfügen, stellt [**shgetfileinfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) eine einfache Möglichkeit zum Abrufen von Informationen zu einem Objekt bereit, das für viele Zwecke ausreicht. **Shgetfileinfo** übernimmt einen voll qualifizierten Pfad oder eine PIDL und gibt eine Vielzahl von Informationen über das Objekt zurück, einschließlich:

-   Der Anzeige Name des Objekts.
-   Die Attribute des Objekts.
-   Handles für die Symbole des Objekts
-   Ein Handle für die System Abbild Liste.
-   Der Pfad der Datei, die das Symbol des Objekts enthält.

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Ein Zeiger auf die IShellFolder-Schnittstelle eines unter Ordners wird erhalten.

Sie können bestimmen, ob der Ordner Unterordner enthält, indem Sie [**IShellFolder:: getattributesof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) aufrufen und überprüfen, ob das sfgao- \_ ordnerflag festgelegt ist. Wenn es sich bei einem Objekt um einen Ordner handelt, können Sie an das Objekt binden, um einen Zeiger auf seine [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle bereitzustellen.

Zum Binden an einen Unterordner müssen Sie die [**IShellFolder:: BindTo Object**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) -Methode des übergeordneten Ordners aufrufen. Diese Methode nimmt die PIDL des unter Ordners an und gibt einen Zeiger auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle zurück. Sobald Sie über diesen Zeiger verfügen, können Sie die **IShellFolder** -Methoden verwenden, um den Inhalt der Unterordner aufzulisten, deren Eigenschaften zu bestimmen usw.

## <a name="determining-an-objects-parent-folder"></a>Bestimmen des übergeordneten Ordners eines Objekts

Wenn Sie über die PIDL eines Objekts verfügen, benötigen Sie möglicherweise ein Handle für eine der Schnittstellen, die vom übergeordneten Ordner verfügbar gemacht werden. Wenn Sie z. b. den mit einer PIDL verknüpften anzeigen Amen mithilfe von [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)bestimmen möchten, müssen Sie zuerst die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des übergeordneten Elements des Objekts abrufen. Dies ist möglich, wenn Sie die in den vorherigen Abschnitten beschriebenen Verfahren verwenden. Ein viel einfacherer Ansatz ist jedoch die Verwendung der Shellfunktion " [**shbindtoparent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent)". Diese Funktion nimmt die voll qualifizierte PIDL eines Objekts an und gibt einen angegebenen Schnittstellen Zeiger für den übergeordneten Ordner zurück. Optional gibt Sie auch die PIDL der einzelnen Ebene des Elements zur Verwendung in Methoden wie [**IShellFolder:: getattributesof**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)zurück.

Mit der folgenden Beispiel Konsolenanwendung wird die PIDL des speziellen System Ordners abgerufen und der Anzeige Name zurückgegeben.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



Die Anwendung verwendet zunächst [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) , um die PIDL des System Ordners abzurufen. Anschließend wird " [**shbindtoparent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent)" aufgerufen, wodurch ein Zeiger auf die [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) -Schnittstelle des übergeordneten Ordners und die PIDL des System Ordners relativ zum übergeordneten Element zurückgegeben wird. Anschließend wird die [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) -Methode des übergeordneten Ordners verwendet, um den anzeigen amen des System Ordners abzurufen. Da **GetDisplayNameOf** eine " [**strinret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) "-Struktur zurückgibt, wird " [**strauretybuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) " verwendet, um den anzeigen Amen in eine normale Zeichenfolge zu konvertieren. Nachdem der Anzeige Name angezeigt wurde, werden die Schnittstellen Zeiger freigegeben und die System-PIDL freigegeben. Beachten Sie, dass die von **shbindtoparent** zurückgegebene relative PIDL nicht freigegeben werden darf.

 

 
