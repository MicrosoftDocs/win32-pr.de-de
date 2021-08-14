---
title: Erstellen von Spaltenhandlern
description: In der Detailansicht im Windows Windows Explorer werden normalerweise mehrere Standardspalten angezeigt.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- Spaltenhandler
- register,column handlers
- Getcolumninfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90876aecdb2626326513723f0cd2c5a6e8f66bfd938b3f56cf10bd3624dd8687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349460"
---
# <a name="creating-column-handlers"></a>Erstellen von Spaltenhandlern

\[Dieses Feature wird nur unter xp Windows oder früher unterstützt. \]

In der Detailansicht im Windows Windows Explorer werden normalerweise mehrere Standardspalten angezeigt. Jede Spalte listet Informationen, z. B. die Dateigröße oder den Typ, für jede Datei im aktuellen Ordner auf. Indem Sie einen Spaltenhandler implementieren und registrieren, können Sie benutzerdefinierte Spalten für die Anzeige verfügbar machen.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shell-Erweiterungshandlers werden unter [Creating Shell Extension Handlers (Erstellen von Shellerweiterungshandlern) erläutert.](/windows/desktop/shell/handlers) Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die spezifisch für Spaltenhandler sind.

Die folgenden Themen werden erläutert.

-   [Funktionsweise von Spaltenhandlern](#how-column-handlers-work)
-   [Registrieren von Spaltenhandlern](#registering-column-handlers)
-   [Implementieren von Spaltenhandlern](#implementing-column-handlers)
    -   [Die Initialize-Methode](#the-initialize-method)
    -   [Die GetColumnInfo-Methode](#the-getcolumninfo-method)
    -   [Die GetItemData-Methode](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Funktionsweise von Spaltenhandlern

Die folgende Abbildung zeigt Windows Explorer in der Detailansicht.

![Screenshot des Windows-Explorers in der Detailansicht](images/columnproviderhandler1.jpg)

Mit Windows 2000 kann der Ordner auch eine Reihe von Spalten unterstützen, die standardmäßig nicht angezeigt werden. Der Benutzer kann zusätzliche Spalten anzeigen, indem er mit der rechten Maustaste auf eine der Spaltenüberschriften klickt und im Menü den Befehl **Mehr...** auswählt. Anschließend wird ein Dialogfeld angezeigt, in dem die verfügbaren Spalten für den Ordner aufgeführt sind und der Benutzer auswählen kann, welche Spalten angezeigt werden sollen. Die folgende Abbildung zeigt dieses Dialogfeld für das vorherige Beispiel.

![Screenshot des Windows-Explorers mit dem angezeigten Dialogfeld "Details auswählen"](images/columnproviderhandler2.jpg)

Durch Erstellen eines Spaltenhandlers können Sie benutzerdefinierte Spalten erstellen und dieser Liste hinzufügen. Beispielsweise könnte eine Sammlung von Dateien, die Musik enthalten, einen Spaltenhandler verwenden, um Spalten anzuzeigen, die den Interpreten und das Stück in den einzelnen Dateien auflisten.

Ein Spaltenhandler ist ein globales Objekt, das jedes Mal aufgerufen wird, wenn Windows Explorer die Detailansicht anzeigt. Spaltenhandler werden jedoch in der Regel verwendet, um benutzerdefinierte Spalten nur für Member eines bestimmten [Dateityps anzuzeigen.](/windows/desktop/shell/fa-file-types) Bevor die Detailansicht angezeigt wird, fragt Windows Explorer alle registrierten Spaltenhandler nach ihren Spaltenmerkmalen ab. Wenn der Benutzer eine der Spalten des Handlers ausgewählt hat, fragt Windows Explorer den Handler nach den zugeordneten Daten ab. Wenn ein Spaltenhandler eine Anforderung für Daten empfängt, stellt er diese zur Verfügung, wenn die Datei ein Member des unterstützten Typs ist. Andernfalls wird die Anforderung ignoriert, indem S \_ FALSE zurückgegeben wird.

## <a name="registering-column-handlers"></a>Registrieren von Spaltenhandlern

Spaltenhandler werden unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Erstellen Sie einen Unterschlüssel von **ColumnHandlers** namens mit der Zeichenfolgenform der KLASSENBEZEICHNER-GUID (CLSID) des Handlers. Eine allgemeine Erörterung des Registrierens von Shell-Erweiterungshandlern finden Sie unter [Creating Shell Extension Handlers](/windows/desktop/shell/handlers). Im folgenden Beispiel wird veranschaulicht, wie ein Spaltenhandler registriert wird.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementieren von Spaltenhandlern

Wie alle Shell-Erweiterungshandler sind Spaltenhandler In-Process-Component Object Model (COM)-Objekte, die als DLLs implementiert sind. Sie exportieren die [**IColumnProvider-Schnittstelle**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) zusätzlich zu [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

Windows Der Explorer ruft die drei methoden auf, die [**von IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) exportiert werden, um die Informationen an fordern, die zum Anzeigen der Spalte benötigt werden. Das verfahren, das vom Windows-Explorer verwendet wird, ist:

1.  Rufen [**Sie IColumnProvider::Initialize auf,**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) um den Ordner anzugeben, der angezeigt werden soll.
2.  Rufen [**Sie IColumnProvider::GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) auf, um den Bezeichner und die Merkmale der Spalte abzurufen.
3.  Wenn die Spalte vom Benutzer ausgewählt wurde, rufen Sie [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) für jede Datei im Ordner auf, um die Daten abzurufen, die in den Spalteneintrag der Datei gehören.

### <a name="the-initialize-method"></a>Die Initialize-Methode

Windows Der Explorer ruft [**IColumnProvider::Initialize auf, um**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) den Spaltenhandler zu initialisieren. Die -Methode verfügt über drei Parameter, derzeit wird jedoch nur *wszFolder* verwendet. Sie wird auf den Ordner festgelegt, dessen Detailansicht angezeigt werden soll. Store den Ordnernamen zur späteren Verwendung an, und initialisieren Sie das Handlerobjekt nach Bedarf.

### <a name="the-getcolumninfo-method"></a>Die GetColumnInfo-Methode

Windows Der Explorer ruft als [**Nächstes IColumnProvider::GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) auf, um den Bezeichner und die Merkmale der Spalte an fordern. Sie übergibt einen Index für die Spalte im *dwIndex-Parameter.* Dieser Index ist ein beliebiger Wert, der zum Aufzählen von Spalten verwendet wird. Windows Explorer übergibt auch einen Zeiger auf eine [**SHCOLUMNINFO-Struktur.**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) Diese Struktur wird verwendet, um den Bezeichner und die Merkmale der Spalte zurück zu geben. **IColumnProvider::GetColumnInfo** sollte den Membern der Struktur entsprechende Werte zuweisen und zurückgeben.

Spalten werden anhand ihrer OLE-Eigenschaftensatz-ID (FMTID) und einer zugeordneten Eigenschaften-ID (PID) identifiziert. Das erste Element der [**SHCOLUMNINFO-Struktur,**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) **scid,** ist ein Zeiger auf eine [**SHCOLUMNID-Struktur,**](/windows/desktop/shell/objects) die zum Identifizieren der Spalte verwendet wird. Das **fmtid-Member** enthält die FMTID der Spalte, und das **pid-Member** enthält die PID der Spalte. Beispielsweise ist ein FMTID-/PID-Standardpaar, das häufig zum Identifizieren von Spalten verwendet wird, die Author PID des Eigenschaftssets Zusammenfassungsinformationen.

Wenn möglich, sollte ihr Handler vorhandene FMTIDs und PIDs verwenden, um die spalte zu identifizieren, die er unterstützt. Wenn Sie eine benutzerdefinierte [**SHCOLUMNID-Struktur**](/windows/desktop/shell/objects) verwenden, zeigt die Spalte nur Daten für die Dateien an, die vom Handler unterstützt werden. Wenn der Ordner andere Dateien enthält, sind die Einträge leer. Wenn ein Ordner Dateien aus mehr als einem Dateityp enthält, kann die Verwendung von FMTID-/PID-Standardwerten das Zusammenführen von Daten aus verschiedenen Typen in derselben Spalte ermöglichen.

Legen Sie **das vt-Member** auf den [**VARIANT-Typ**](/windows/win32/api/oaidl/ns-oaidl-variant) der Daten fest, die Sie in der Spalte anzeigen möchten. Der am häufigsten verwendete Typ ist VT LPSTR, da die meisten Spalten \_ ihre Daten als Zeichenfolgen anzeigen. Die verbleibenden Elemente der [**SHCOLUMNINFO-Struktur**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) werden verwendet, um die Merkmale der Spalte zu definieren. Weisen Sie werte entsprechend zu.

### <a name="the-getitemdata-method"></a>Die GetItemData-Methode

Wenn die Spalte des Spaltenhandlers ausgewählt wurde, ruft Windows Explorer [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) für jede Datei in dem Ordner auf, der angezeigt werden soll. Der *pscid-Parameter* ist ein Zeiger auf eine [**SHCOLUMNID-Struktur,**](/windows/desktop/shell/objects) die die Spalte identifiziert. Der *pscd-Parameter* verweist auf eine [**SHCOLUMNDATA-Struktur,**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) die die bestimmte Datei identifiziert.

Der *pvarData-Parameter* gibt die Daten zurück, die in der -Spalte des Handlers für die durch *pscd* angegebene Datei angezeigt werden sollen. Wenn diese Datei vom Spaltenhandler unterstützt wird, weisen Sie ihren Datenwert *pvarData* zu, und geben Sie S \_ OK zurück. Wenn die Datei von Ihrem Spaltenhandler nicht unterstützt wird, geben Sie S FALSE zurück, ohne \_ *pvarData* einen Wert zu zuweisen.

Viele Ordner enthalten eine Reihe von Dateien, die von einem bestimmten Spaltenhandler nicht unterstützt werden. Um die Effizienz zu verbessern, sollte [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) zuerst den **pwszExt-Member** der Struktur überprüfen, auf die *pscd zeigt.* Dieser Member enthält die Dateinamenerweiterung. Wenn die Erweiterung angibt, dass die Datei kein Member eines vom Handler unterstützten Dateityps ist, vermeiden Sie unnötige Verarbeitung, indem Sie sofort S \_ FALSE zurückgeben.

 

 