---
title: Erstellen von Spalten Handlern
description: In der Detailansicht in Windows-Explorer werden normalerweise mehrere Standard Spalten angezeigt.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- Spalten Handler
- registrieren, Spalten Handler
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940796e75f29ba0fcfa025d9a56267e14bdff38f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104565664"
---
# <a name="creating-column-handlers"></a>Erstellen von Spalten Handlern

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. \]

In der Detailansicht in Windows-Explorer werden normalerweise mehrere Standard Spalten angezeigt. In jeder Spalte sind Informationen, z. b. die Dateigröße oder der Datentyp, für jede Datei im aktuellen Ordner aufgelistet. Durch Implementieren und Registrieren eines Spalten Handlers können Sie benutzerdefinierte Spalten zur Anzeige verfügbar machen.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](/windows/desktop/shell/handlers)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Spalten Handler spezifisch sind.

Die folgenden Themen werden erörtert.

-   [Funktionsweise von Spalten Handlern](#how-column-handlers-work)
-   [Registrieren von Spalten Handlern](#registering-column-handlers)
-   [Implementieren von Spalten Handlern](#implementing-column-handlers)
    -   [Die Initialize-Methode](#the-initialize-method)
    -   [Die GetColumnInfo-Methode](#the-getcolumninfo-method)
    -   [Die GetItemData-Methode](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Funktionsweise von Spalten Handlern

Die folgende Abbildung zeigt den Windows-Explorer in der Detailansicht.

![Screenshot von Windows-Explorer in der Detailansicht](images/columnproviderhandler1.jpg)

Mit Windows 2000 kann der Ordner auch eine Reihe von Spalten unterstützen, die standardmäßig nicht angezeigt werden. Der Benutzer kann weitere Spalten anzeigen, indem Sie mit der rechten Maustaste auf einen der Spaltenüberschriften klicken und im Menü den Befehl **Weitere...** auswählen. Daraufhin wird ein Dialogfeld angezeigt, in dem die für den Ordner verfügbaren Spalten aufgeführt sind, und der Benutzer kann auswählen, welche Spalten angezeigt werden sollen. Die folgende Abbildung zeigt dieses Dialogfeld für das vorherige Beispiel.

![Screenshot von Windows-Explorer mit dem angezeigten Dialogfeld "Details auswählen"](images/columnproviderhandler2.jpg)

Durch Erstellen eines Spalten Handlers können Sie benutzerdefinierte Spalten erstellen und diese dieser Liste hinzufügen. Eine Auflistung von Dateien, die Musik enthalten, könnte z. b. einen Spalten Handler zum Anzeigen von Spalten verwenden, in denen der in jeder Datei enthaltene Teil des Künstlers und des Stückes aufgeführt ist

Ein Spalten Handler ist ein globales Objekt, das jedes Mal aufgerufen wird, wenn Windows Explorer die Detailansicht anzeigt. Spalten Handler werden jedoch normalerweise verwendet, um benutzerdefinierte Spalten nur für Member eines bestimmten [Dateityps](/windows/desktop/shell/fa-file-types)anzuzeigen. Bevor die Detailansicht angezeigt wird, fragt Windows Explorer alle registrierten Spalten Handler nach den Spalten Merkmalen ab. Wenn der Benutzer eine der Spalten des Handlers ausgewählt hat, fragt Windows Explorer den Handler nach den zugeordneten Daten ab. Wenn ein Spalten Handler eine Anforderung für Daten empfängt, wird er bereitstellt, wenn die Datei ein Member des unterstützten Typs ist. Andernfalls wird die Anforderung ignoriert, indem S false zurückgegeben wird \_ .

## <a name="registering-column-handlers"></a>Registrieren von Spalten Handlern

Spalten Handler werden unter dem folgenden Unterschlüssel registriert.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Erstellen Sie einen Unterschlüssel von **columnhandlers** , der mit der Zeichen folgen Form der Klassen Bezeichner-GUID (CLSID) des Handlers benannt ist. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](/windows/desktop/shell/handlers). Das folgende Beispiel veranschaulicht das Registrieren eines Spalten Handlers.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementieren von Spalten Handlern

Wie bei allen Shellerweiterungs Handlern sind Spalten Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Sie exportieren die [**icolumnprovider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) -Schnittstelle zusätzlich zu [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

Windows-Explorer Ruft die drei von [**icolumnprovider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) exportierten Methoden auf, um die Informationen anzufordern, die zum Anzeigen der Spalte benötigt werden. Der Windows-Explorer verwendet Folgendes:

1.  Nennen Sie [**icolumnprovider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) , um den Ordner anzugeben, der angezeigt werden soll.
2.  Rufen Sie [**icolumnprovider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) auf, um den Bezeichner und die Merkmale der Spalte abzurufen.
3.  Wenn die Spalte vom Benutzer ausgewählt wurde, rufen Sie [**icolumnprovider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) für jede Datei im Ordner auf, um die Daten abzurufen, die zu dem Spalten Eintrag der Datei gehören.

### <a name="the-initialize-method"></a>Die Initialize-Methode

In Windows Explorer wird [**icolumnprovider:: Initialisieren**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) aufgerufen, um den Spalten Handler zu initialisieren. Die-Methode verfügt über drei Parameter, aber zurzeit wird nur *wszfolder* verwendet. Sie wird auf den Ordner festgelegt, dessen Detailansicht angezeigt wird. Speichern Sie den Ordnernamen für die spätere Verwendung, und initialisieren Sie das Handlerobjekt nach Bedarf.

### <a name="the-getcolumninfo-method"></a>Die GetColumnInfo-Methode

Windows Explorer Next ruft [**icolumnprovider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) auf, um den Bezeichner und die Merkmale der Spalte anzufordern. Sie übergibt einen Index für die Spalte im *dwIndex* -Parameter. Dieser Index ist ein beliebiger Wert, der zum Aufzählen von Spalten verwendet wird. Windows-Explorer übergibt auch einen Zeiger auf eine [**shcolumninfo**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) -Struktur. Diese Struktur wird verwendet, um den Bezeichner und die Merkmale der Spalte zurückzugeben. **Icolumnprovider:: GetColumnInfo** sollte den Membern der Struktur geeignete Werte zuweisen und zurückgeben.

Spalten werden durch ihre OLE-Eigenschafts Satz-ID (fmtid) und eine zugehörige Eigenschaften-ID (PID) identifiziert. Der erste Member der [**shcolumninfo**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) -Struktur, **scid**, ist ein Zeiger auf eine [**shcolumnid**](/windows/desktop/shell/objects) -Struktur, die zum Identifizieren der Spalte verwendet wird. Der **fmtid** -Member der Spalte enthält die fmtid der Spalte, und sein **PID** -Element enthält die PID der Spalte. Beispielsweise ist ein Standardmäßiges fmtid/PID-Paar, das häufig verwendet wird, um Spalten zu identifizieren, die Autor-PID des Eigenschaften Satzes für Zusammenfassungs Informationen.

Wenn möglich, sollte der Handler vorhandene fmtids und PIDs verwenden, um die unterstützte Spalte zu identifizieren. Wenn Sie eine benutzerdefinierte [**shcolumnid**](/windows/desktop/shell/objects) -Struktur verwenden, werden in der Spalte nur Daten für die Dateien angezeigt, die vom Handler unterstützt werden. Wenn der Ordner andere Dateien enthält, sind die Einträge leer. Wenn ein Ordner Dateien aus mehr als einem Dateityp enthält, kann das Zusammenführen von Daten aus unterschiedlichen Typen in derselben Spalte durch die Verwendung von Standard-fmtid/pid-Werten möglich sein.

Legen Sie das **VT** -Element auf den [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)-Typ der Daten fest, die   Sie in der Spalte anzeigen möchten. Der am häufigsten verwendete Typ ist VT \_ LPStr, da die meisten Spalten Ihre Daten als Zeichen folgen anzeigen. Die übrigen Member der [**shcolumninfo**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) -Struktur werden verwendet, um die Merkmale der Spalte zu definieren. Weisen Sie Werte nach Bedarf zu.

### <a name="the-getitemdata-method"></a>Die GetItemData-Methode

Wenn die Spalte des Spalten Handlers ausgewählt wurde, ruft Windows-Explorer [**icolumnprovider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) für jede Datei im Ordner auf, der angezeigt werden soll. Der *pscid-* Parameter ist ein Zeiger auf eine [**shcolumnid**](/windows/desktop/shell/objects) -Struktur, die die Spalte identifiziert. Der *PSCD-* Parameter verweist auf eine [**shcolumndata**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) -Struktur, die die jeweilige Datei identifiziert.

Der *pvardata* -Parameter gibt die Daten zurück, die in der Spalte des Handlers für die durch *PSCD* angegebene Datei angezeigt werden sollen. Wenn diese Datei von Ihrem Spalten Handler unterstützt wird, weisen Sie *pvardata* den Datenwert zu, und geben Sie "S OK" zurück \_ . Wenn die Datei nicht vom Spalten Handler unterstützt wird, geben Sie S false zurück, \_ ohne *pvardata* einen Wert zuzuweisen.

Viele Ordner enthalten eine Reihe von Dateien, die von keinem bestimmten Spalten Handler unterstützt werden. Um die Effizienz zu verbessern, sollte [**icolumnprovider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) zuerst den **pwszext** -Member der Struktur überprüfen, auf die von *PSCD* verwiesen wird. Dieser Member enthält die Dateinamenerweiterung. Wenn die Erweiterung angibt, dass die Datei kein Member eines Dateityps ist, der vom Handler unterstützt wird, sollten Sie unnötige Verarbeitung vermeiden, indem Sie den Wert "false" zurückgeben \_ .

 

 