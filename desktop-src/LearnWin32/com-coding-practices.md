---
title: COM-Codierungs Methoden
description: In diesem Thema wird beschrieben, wie Sie Ihren com-Code effektiver und robuster gestalten können.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102478"
---
# <a name="com-coding-practices"></a>COM-Codierungs Methoden

In diesem Thema wird beschrieben, wie Sie Ihren com-Code effektiver und robuster gestalten können.

-   [Der \_ \_ uuidof-Operator](/windows)
-   [Das IID \_ PPV \_ args-Makro](/windows)
-   [Das saferelease-Muster](#the-saferelease-pattern)
-   [Intelligente com-Zeiger](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>Der \_ \_ uuidof-Operator

Wenn Sie das Programm erstellen, erhalten Sie möglicherweise Linker-Fehler ähnlich den folgenden:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Dieser Fehler bedeutet, dass eine GUID-Konstante mit externer Verknüpfung (**extern**) deklariert wurde und der Linker die Definition der Konstante nicht finden konnte. Der Wert einer GUID-Konstante wird in der Regel aus einer statischen Bibliotheksdatei exportiert. Wenn Sie Microsoft Visual C++ verwenden, können Sie vermeiden, dass eine statische Bibliothek mit dem **\_ \_ uuidof** -Operator verknüpft werden muss. Dieser Operator ist eine Microsoft-Spracherweiterung. Er gibt einen GUID-Wert aus einem Ausdruck zurück. Der Ausdruck kann ein Schnittstellentyp Name, ein Klassenname oder ein Schnittstellen Zeiger sein. Mithilfe von **\_ \_ uuidof** können Sie das gemeinsame Element Dialog Objekt wie folgt erstellen:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Der Compiler extrahiert den GUID-Wert aus dem Header, sodass kein Bibliotheks Export notwendig ist.

> [!Note]  
> Der GUID-Wert wird durch Deklarieren im-Header dem Typnamen zugeordnet `__declspec(uuid( ... ))` . Weitere Informationen finden Sie in der Dokumentation zu **\_ \_ declspec** in der Visual C++-Dokumentation.

 

## <a name="the-iid_ppv_args-macro"></a>Das IID \_ PPV \_ args-Makro

Wir haben gesehen, dass sowohl [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) als auch [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) das Umwandeln des letzten Parameters in einen **void \* \*** -Typ erfordern. Dadurch wird das Potenzial eines Typen Konflikts erstellt. Betrachten Sie das folgende Codefragment:


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



Dieser Code fordert die [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Schnittstelle an, übergibt aber einen [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Zeiger. Der **reinterpretierungscast \_** -Ausdruck umgeht das C++-Typsystem, sodass der Compiler diesen Fehler nicht abfängt. Im besten Fall, wenn das Objekt die angeforderte Schnittstelle nicht implementiert, schlägt der-Befehl einfach fehl. Im schlimmsten Fall ist die Funktion erfolgreich, und Sie verfügen über einen nicht übereinstimmenden Zeiger. Anders ausgedrückt: der Zeigertyp stimmt nicht mit der tatsächlichen Vtable im Arbeitsspeicher. Wie Sie sich vorstellen können, kann an dieser Stelle nichts gutes vorkommen.

> [!Note]  
> Eine *vtable* (Virtual Method Table) ist eine Tabelle mit Funktions Zeigern. Die Vtable-Methode gibt an, wie com einen Methodenaufruf an seine Implementierung zur Laufzeit bindet. Nicht zufällig stellen vtables dar, wie die meisten C++-Compiler virtuelle Methoden implementieren.

 

Das [**IID \_ PPV \_ args**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) -Makro hilft, diese Fehler Klasse zu vermeiden. Um dieses Makro zu verwenden, ersetzen Sie den folgenden Code:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



durch diesen:


```C++
IID_PPV_ARGS(&pFileOpen)
```



Das Makro fügt automatisch `__uuidof(IFileOpenDialog)` für den Schnittstellen Bezeichner ein, sodass es sicher ist, dass es mit dem Zeigertyp identisch ist. Dies ist der geänderte (und korrekte) Code:


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Sie können dasselbe Makro mit [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))verwenden:


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>Das saferelease-Muster

Die Verweis Zählung ist eine der Dinge in der Programmierung, die im Grunde einfach ist, aber auch mühsam ist, sodass es leicht schief geht. Typische Fehler sind:

-   Ein Schnittstellen Zeiger kann nicht freigegeben werden, wenn Sie ihn nicht mehr verwenden. Diese Fehler Klasse bewirkt, dass Ihr Programmspeicher und andere Ressourcen nicht mehr unternimmt, da Objekte nicht zerstört werden.
-   [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) mit einem ungültigen Zeiger wird aufgerufen. Dieser Fehler kann z. b. auftreten, wenn das Objekt nie erstellt wurde. Diese Fehler Kategorie führt wahrscheinlich zu einem Absturz Ihres Programms.
-   Dereferenzierung eines Schnittstellen Zeigers nach dem Aufrufen des [**Releases**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) . Dieser Fehler kann zum Absturz des Programms führen. Schlimmer noch: das Programm kann zu einem zufälligen späteren Zeitpunkt abstürzen, sodass es schwierig ist, den ursprünglichen Fehler zu finden.

Eine Möglichkeit, diese Fehler zu vermeiden, besteht darin, die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) über eine Funktion aufzurufen, die den Zeiger sicher freigibt. Der folgende Code zeigt eine Funktion, die Folgendes bewirkt:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



Diese Funktion verwendet einen COM-Schnittstellen Zeiger als Parameter und führt folgende Aktionen aus:

1.  Überprüft, ob der Zeiger **null** ist.
2.  Ruft [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, wenn der Zeiger nicht **null** ist.
3.  Legt den Zeiger auf **null** fest.

Im folgenden finden Sie ein Beispiel für die Verwendung von `SafeRelease` :


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



Wenn [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erfolgreich ist, gibt der-Befehl `SafeRelease` den-Zeiger frei. Wenn **cokreateingestance** fehlschlägt, bleibt *pfileopen* gleich **null**. Die `SafeRelease` Funktion prüft dies und überspringt den [**Freigabe Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)Vorgang.

Es ist auch sicher, mehrmals `SafeRelease` auf demselben Zeiger aufzurufen, wie hier gezeigt:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Intelligente com-Zeiger

Die- `SafeRelease` Funktion ist nützlich, erfordert jedoch zwei Dinge:

-   Initialisieren Sie jeden Schnittstellen Zeiger auf **null**.
-   Wird aufgerufen `SafeRelease` , bevor jeder Zeiger den Gültigkeitsbereich verlässt.

Als C++-Programmierer denken Sie wahrscheinlich daran, dass Sie sich keine dieser Dinge merken müssen. Das ist der Grund, warum C++ über Konstruktoren und Dekonstruktoren verfügt. Es wäre schön, eine Klasse zu haben, die den zugrunde liegenden Schnittstellen Zeiger umschließt und den Zeiger automatisch initialisiert und freigibt. Anders ausgedrückt, wir möchten etwa Folgendes:


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



Die hier gezeigte Klassendefinition ist unvollständig und kann nicht wie dargestellt verwendet werden. Sie müssen mindestens einen Kopierkonstruktor, einen Zuweisungs Operator und eine Möglichkeit für den Zugriff auf den zugrunde liegenden COM-Zeiger definieren. Glücklicherweise müssen Sie keine dieser Aufgaben erledigen, da Microsoft Visual Studio bereits eine intelligente Zeiger Klasse als Teil der Active Template Library (ATL) bereitstellt.

Die intelligente ATL-Zeiger Klasse hat den Namen " **CComPtr**". (Es gibt auch eine **CComQIPtr** -Klasse, die hier nicht erläutert wird.) Hier sehen Sie das [Dialog Feld Öffnen](example--the-open-dialog-box.md) , das für die Verwendung von **CComPtr** umgeschrieben wird.


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



Der Hauptunterschied zwischen diesem Code und dem ursprünglichen Beispiel besteht darin, dass diese Version [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)nicht explizit aufruft. Wenn die **CComPtr** -Instanz den Gültigkeitsbereich verlässt, ruft der Dekonstruktor **Release** auf dem zugrunde liegenden Zeiger auf.

**CComPtr** ist eine Klassen Vorlage. Das Vorlagen Argument ist der com-Schnittstellentyp. Intern enthält **CComPtr** einen Zeiger dieses Typs. **CComPtr** überschreibt **Operator-> ()** und **Operator& ()** , sodass die Klasse wie der zugrunde liegende Zeiger fungiert. Beispielsweise entspricht der folgende Code dem direkten Aufrufen der **IFileOpenDialog:: Show** -Methode:


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr** definiert auch eine **CComPtr:: cokreatan Stance** -Methode, die die com- [**cokreateinzustance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion mit einigen Standardparameterwerten aufruft. Der einzige erforderliche Parameter ist der Klassen Bezeichner, wie im folgenden Beispiel gezeigt:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



Die **CComPtr:: cokreateinzustance** -Methode wird ausschließlich als praktische bereitgestellt. Wenn Sie möchten, können Sie weiterhin die com- [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen.

## <a name="next"></a>Nächste

[Fehlerbehandlung in com](error-handling-in-com.md)

 

 