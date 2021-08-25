---
title: COM-Codierungsmethoden
description: In diesem Thema werden Möglichkeiten beschrieben, ihren COM-Code effektiver und stabiler zu gestalten.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93febc4ee3dfd4f05f20fae8078bc2a5ebb7f9623a860f49ec9cd6ce4e69b95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913889"
---
# <a name="com-coding-practices"></a>COM-Codierungsmethoden

In diesem Thema werden Möglichkeiten beschrieben, ihren COM-Code effektiver und stabiler zu gestalten.

-   [Der \_ \_ uuidof-Operator](/windows)
-   [Das IID \_ PPV \_ ARGS-Makro](/windows)
-   [SafeRelease-Muster](#the-saferelease-pattern)
-   [Intelligente COM-Zeiger](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a>Der \_ \_ uuidof-Operator

Wenn Sie Ihr Programm erstellen, erhalten Sie möglicherweise Linkerfehler wie die folgenden:

`unresolved external symbol "struct _GUID const IID_IDrawable"`

Dieser Fehler bedeutet, dass eine GUID-Konstante mit externer Verknüpfung **(extern)** deklariert wurde und der Linker die Definition der Konstante nicht finden konnte. Der Wert einer GUID-Konstante wird normalerweise aus einer statischen Bibliotheksdatei exportiert. Wenn Sie Microsoft Visual C++ verwenden, können Sie vermeiden, dass eine statische Bibliothek mithilfe des **\_ \_ uuidof-Operators verlinkt werden** muss. Dieser Operator ist eine Microsoft-Spracherweiterung. Sie gibt einen GUID-Wert aus einem Ausdruck zurück. Der Ausdruck kann ein Schnittstellentypname, ein Klassenname oder ein Schnittstellenzeiger sein. Mit **\_ \_ uuidof** können Sie das Common Item Dialog-Objekt wie folgt erstellen:


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



Der Compiler extrahiert den GUID-Wert aus dem Header, sodass kein Bibliotheksexport erforderlich ist.

> [!Note]  
> Der GUID-Wert wird dem Typnamen durch Deklarieren `__declspec(uuid( ... ))` im Header zugeordnet. Weitere Informationen finden Sie in der Dokumentation zu **\_ \_ declspec** in der Visual C++ Dokumentation.

 

## <a name="the-iid_ppv_args-macro"></a>Das IID \_ PPV \_ ARGS-Makro

Wir haben gesehen, dass [**sowohl CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) als auch [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) das Umleiten des letzten Parameters in einen **void-Typ \* \*** erfordern. Dadurch entsteht das Potenzial für einen Typkonflikt. Betrachten Sie das folgende Codefragment:


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



Dieser Code fragt nach der [**IFileDialogCustomize-Schnittstelle,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) übergibt jedoch einen [**IFileOpenDialog-Zeiger.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Der **neu interpretierte \_ Cast-Ausdruck** umgeht das C++-Typsystem, sodass der Compiler diesen Fehler nicht abfing. Wenn das Objekt die angeforderte Schnittstelle nicht implementiert, schlägt der Aufruf im besten Fall einfach fehl. Im schlimmsten Fall ist die Funktion erfolgreich, und Sie verfügen über einen nicht übereinstimmenden Zeiger. Anders ausgedrückt: Der Zeigertyp ist nicht mit der tatsächlichen vtable im Arbeitsspeicher übereinstimmen. Wie Sie sich vorstellen können, kann an diesem Punkt nichts Gutes passieren.

> [!Note]  
> Eine *vtable* (virtuelle Methodentabelle) ist eine Tabelle mit Funktionsze0ern. Die vtable ist die Art und Weise, in der COM einen Methodenaufruf zur Laufzeit an seine Implementierung bindet. VTables sind nicht zufällig, wie die meisten C++-Compiler virtuelle Methoden implementieren.

 

Das [**IID \_ PPV \_ ARGS-Makro**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) hilft, diese Fehlerklasse zu vermeiden. Ersetzen Sie den folgenden Code, um dieses Makro zu verwenden:


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



durch diesen:


```C++
IID_PPV_ARGS(&pFileOpen)
```



Das Makro fügt automatisch für den Schnittstellenbezeichner ein, sodass es garantiert `__uuidof(IFileOpenDialog)` mit dem Zeigertyp übereinstimmen kann. Hier ist der geänderte (und richtige) Code:


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



Sie können das gleiche Makro mit [**QueryInterface verwenden:**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a>SafeRelease-Muster

Die Verweiszählung ist eine der Dinge in der Programmierung, die im Grunde einfach, aber auch mühsam ist, was es einfach macht, falsch zu werden. Typische Fehler sind:

-   Fehler beim Veröffentlichen eines Schnittstellenzeigers, wenn Sie ihn nicht mehr verwenden. Diese Fehlerklasse verursacht, dass ihr Programm Arbeitsspeicher und andere Ressourcen aussicd, da Objekte nicht zerstört werden.
-   Aufrufen [**von Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) mit einem ungültigen Zeiger. Dieser Fehler kann beispielsweise vorkommen, wenn das Objekt nie erstellt wurde. Diese Fehlerkategorie wird wahrscheinlich dazu führen, dass Ihr Programm abstürzt.
-   Deeferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called. Dieser Fehler kann dazu führen, dass Ihr Programm abstürzt. Noch schlechter ist, dass ihr Programm zu einem späteren Zeitpunkt nach dem Zufallsprinzip abstürzt, wodurch es schwierig ist, den ursprünglichen Fehler zu finden.

Eine Möglichkeit, diese Fehler zu vermeiden, besteht im Aufrufen von [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) über eine Funktion, die den Zeiger sicher frei gibt. Der folgende Code zeigt eine Funktion, die dies tut:


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



Diese Funktion verwendet einen COM-Schnittstellenzeiger als Parameter und führt Folgendes aus:

1.  Überprüft, ob der Zeiger NULL **ist.**
2.  Ruft [**Release auf,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) wenn der Zeiger nicht **NULL ist.**
3.  Legt den Zeiger auf **NULL fest.**

Hier ist ein Beispiel für die Verwendung von `SafeRelease` :


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



Wenn [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erfolgreich ist, gibt der Aufruf von `SafeRelease` den Zeiger frei. Wenn **CoCreateInstance fehlschlägt,** *bleibt pFileOpen* **NULL.** Die `SafeRelease` Funktion überprüft dies und überspringt den Aufruf von [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).

Es ist auch sicher, mehrere Aufrufe für denselben Zeiger zu `SafeRelease` führen, wie hier gezeigt:


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a>Intelligente COM-Zeiger

Die `SafeRelease` Funktion ist nützlich, aber Sie müssen sich zwei Dinge merken:

-   Initialisieren Sie jeden Schnittstellenzeiger auf **NULL.**
-   Rufen `SafeRelease` Sie auf, bevor jeder Zeiger den Gültigkeitsbereich übergeht.

Als C++-Programmierer denken Sie wahrscheinlich, dass Sie sich keines dieser Dinge merken sollten. Das ist schließlich der Grund, warum C++ Konstruktoren und Destruktoren hat. Es wäre gut, eine Klasse zu verwenden, die den zugrunde liegenden Schnittstellenzeiger umschließt und den Zeiger automatisch initialisiert und freilässt. Anders ausgedrückt: Wir möchten etwas wie das:


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



Die hier gezeigte Klassendefinition ist unvollständig und kann nicht wie gezeigt verwendet werden. Sie müssen mindestens einen Kopierkonstruktor, einen Zuweisungsoperator und eine Möglichkeit für den Zugriff auf den zugrunde liegenden COM-Zeiger definieren. Glücklicherweise müssen Sie diese Arbeit nicht tun, da Microsoft Visual Studio bereits eine intelligente Zeigerklasse als Teil des Active Template Library (ATL) bietet.

Die intelligente ATL-Zeigerklasse heißt **CComPtr.** (Es gibt auch eine **CComQIPtr-Klasse,** die hier nicht erläutert wird.) Im folgenden Beispiel wird [dialogfeld öffnen umgeschrieben,](example--the-open-dialog-box.md) um **CComPtr zu verwenden.**


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



Der Hauptunterschied zwischen diesem Code und dem ursprünglichen Beispiel ist, dass diese Version release nicht explizit [**aufruft.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) Wenn die **CComPtr-Instanz** den Gültigkeitsbereich übergeht, ruft der Destruktor **Release** für den zugrunde liegenden Zeiger auf.

**CComPtr ist** eine Klassenvorlage. Das Vorlagenargument ist der COM-Schnittstellentyp. Intern enthält **CComPtr** einen Zeiger dieses Typs. **CComPtr** überschreibt **operator->()** und **operator&(), sodass** die Klasse wie der zugrunde liegende Zeiger fungiert. Der folgende Code entspricht beispielsweise dem direkten Aufrufen der **IFileOpenDialog::Show-Methode:**


```C++
hr = pFileOpen->Show(NULL);
```



**CComPtr definiert** auch eine **CComPtr::CoCreateInstance-Methode,** die die COM [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit einigen Standardparameterwerten aufruft. Der einzige erforderliche Parameter ist der Klassenbezeichner, wie im nächsten Beispiel gezeigt:


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



Die **CComPtr::CoCreateInstance-Methode** wird ausschließlich zur Vereinfachung bereitgestellt. Sie können weiterhin die [**COM-Funktion CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, wenn Sie dies bevorzugen.

## <a name="next"></a>Nächste

[Fehlerbehandlung in COM](error-handling-in-com.md)

 

 