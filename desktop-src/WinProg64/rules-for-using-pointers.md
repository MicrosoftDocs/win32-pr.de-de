---
title: Regeln für die Verwendung von Zeigern
description: Das Portieren von Code für die Kompilierung von Microsoft Windows 32-und 64-Bit ist unkompliziert. Sie müssen nur einige einfache Regeln zum Umwandeln von Zeigern befolgen und die neuen Datentypen in Ihrem Code verwenden. Die Regeln für die Zeiger Bearbeitung lauten wie folgt.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- Regeln für die Verwendung von Zeigern 64-Bit-Windows-Programmierung
- Zeiger Manipulation 64-Bit-Windows-Programmierung
- Umwandeln von Zeigern 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103949185"
---
# <a name="rules-for-using-pointers"></a>Regeln für die Verwendung von Zeigern

Das Portieren von Code für die Kompilierung von Microsoft Windows 32-und 64-Bit ist unkompliziert. Sie müssen nur einige einfache Regeln zum Umwandeln von Zeigern befolgen und die neuen Datentypen in Ihrem Code verwenden. Die Regeln für die Zeiger Bearbeitung lauten wie folgt.

1.  Verwenden Sie keine Zeiger in **int**, **Long**, **ulong** oder **DWORD**.

    Wenn Sie einen Zeiger umwandeln müssen, um einige Bits zu testen, Bits festzulegen oder zu löschen oder den Inhalt anderweitig zu bearbeiten, verwenden Sie den **uint- \_ ptr** -oder den **int- \_ ptr** -Typ. Bei diesen Typen handelt es sich um ganzzahlige Typen, die auf die Größe eines Zeigers für 32-und 64-Bit-Fenster skaliert werden (z. b. **ulong** für 32-Bit-Windows und \_ Int64 für 64-Bit-Windows). Nehmen Sie beispielsweise an, dass Sie den folgenden Code portieren:

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Im Rahmen des Portierungs Prozesses ändern Sie den Code wie folgt:

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Verwenden Sie ggf. **uint \_ ptr** und **int \_ ptr** (und wenn Sie unsicher sind, ob Sie erforderlich sind, gibt es keinen Schaden bei der Verwendung in der Groß-/Kleinschreibung). Wandeln Sie Ihre Zeiger nicht in die Typen **ulong**, **Long**, **int**, **uint** oder **DWORD** um.

    Beachten Sie, dass **handle** als **void \*** definiert ist, sodass ein **handle** -Wert für einen **ulong** -Wert zum Testen, festlegen oder Löschen der niedrig wertigen 2 Bits in 64-Bit-Fenstern ein Fehler ist.

2.  Verwenden Sie die **ptrtolong** -oder **ptrtoulong** -Funktion, um Zeiger zu kürzen.

    Wenn Sie einen Zeiger auf einen 32-Bit-Wert kürzen müssen, verwenden Sie die **ptrtolong** -oder **ptrtoulong** -Funktion (in basetsd. h definiert). Diese Funktionen deaktivieren die zeigertrunzierungswarnung für die Dauer des Aufrufes.

    Verwenden Sie diese Funktionen sorgfältig. Nachdem Sie eine Zeiger Variable mithilfe einer dieser Funktionen konvertiert haben, verwenden Sie Sie nie erneut als Zeiger. Diese Funktionen kürzen die oberen 32 Bits einer Adresse, die normalerweise benötigt werden, um auf den Speicher zuzugreifen, auf den ursprünglich durch Zeiger verwiesen wird. Wenn Sie diese Funktionen ohne sorgfältige Überlegung verwenden, führt dies zu zerbrechlichem Code.

3.  Seien Sie vorsichtig, wenn Sie Zeiger \_ 32-Werte in Code verwenden, die als 64-Bit-Code kompiliert werden können. Der Compiler signiert den Zeiger, wenn er einem systemeigenen Zeiger im 64-Bit-Code zugewiesen wird, und nicht mit 0 (null).
4.  Seien Sie vorsichtig, wenn Sie Zeiger \_ 64-Werte in Code verwenden, die als 32-Bit-Code kompiliert werden können. Der Compiler signiert den Zeiger im 32-Bit-Code und erweitert den Zeiger nicht mit NULL.
5.  Achten Sie darauf, out-Parameter zu verwenden.

    Angenommen, Sie haben eine Funktion wie folgt definiert:

    `void func( OUT PULONG *PointerToUlong );`

    Diese Funktion kann nicht wie folgt aufgerufen werden.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    Verwenden Sie stattdessen den folgenden-Befehl.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Typecasting &UL auf **Pulong \*** verhindert einen Compilerfehler, aber die Funktion schreibt einen 64-Bit-Zeiger Wert in den Arbeitsspeicher &UL. Dieser Code funktioniert auf 32-Bit-Fenstern, führt jedoch zu Daten Beschädigungen auf 64-Bit-Fenstern und ist eine feine, schwer zu suchende Beschädigung. In der untersten Zeile: spielen Sie keine Tricks mit dem C-Code. – unkompliziert und einfach ist besser.

6.  Seien Sie vorsichtig mit polymorphen Schnittstellen.

    Erstellen Sie keine Funktionen, die **DWORD** -Parameter für polymorphe Daten akzeptieren. Wenn die Daten ein Zeiger oder ein ganzzahliger Wert sein können, verwenden Sie den uint- \_ Typ PTR oder **pVoid** .

    Erstellen Sie z. b. keine Funktion, die ein Array von Ausnahme Parametern akzeptiert, die als **DWORD** -Werte typisiert sind. Das Array muss ein Array von **DWORD- \_ ptr** -Werten sein. Daher können die Array Elemente Adressen oder ganzzahlige 32-Bit-Werte enthalten. (Die allgemeine Regel ist, dass, wenn der ursprüngliche Typ **DWORD** ist und es sich um eine Zeiger Breite handeln muss, in einen **DWORD- \_ ptr** -Wert konvertiert wird. Daher gibt es entsprechende Typen von Zeiger Genauigkeit.) Wenn Sie über Code verfügen, der **DWORD**-, **ulong**-oder andere 32-Bit-Typen in polymorph-Weise verwendet (d. h., Sie möchten, dass der Parameter oder der Strukturmember eine Adresse enthält), verwenden Sie **uint \_ ptr** anstelle des aktuellen Typs.

7.  Verwenden Sie die neuen Fenster Klassen Funktionen.

    Wenn Sie über private Fenster-oder Klassen Daten verfügen, die Zeiger enthalten, muss der Code die folgenden neuen Funktionen verwenden:

    -   [**Getclasslongptr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**Getwindowlongptr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**Setclasslongptr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**Setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    Diese Funktionen können in 32-und 64-Bit-Fenstern verwendet werden, sind jedoch auf 64-Bit-Windows erforderlich. Bereiten Sie sich auf den Übergang vor, indem Sie diese Funktionen jetzt verwenden.

    Außerdem müssen Sie auf Zeiger oder Handles in der Klasse private Daten zugreifen, indem Sie die neuen Funktionen auf 64-Bit-Windows verwenden. Die folgenden Indizes werden bei einer 64-Bit-Kompilierung nicht in winuser. h definiert, um Sie bei der Suche nach diesen Fällen zu unterstützen:

    -   GWL \_ WndProc
    -   GWL- \_ HINSTANCE
    -   GWL \_ hwdparent
    -   GWL \_ User Data

    Stattdessen definiert Winuser. h die folgenden neuen Indizes:

    -   gwlp \_ WndProc
    -   gwlp \_ HINSTANCE
    -   gwlp \_ hwndParent
    -   gwlp \_ UserData
    -   gwlp- \_ ID

    Der folgende Code wird z. b. nicht kompiliert:

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Er sollte wie folgt geändert werden:

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Wenn Sie das **CbWndExtra** -Element der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur festlegen, stellen Sie sicher, dass genügend Speicherplatz für Zeiger reserviert ist. Wenn Sie z. b. gerade sizeof-bytes (DWORD) für einen Zeiger Wert reservieren, reservieren Sie sizeof-bytes (DWORD \_ PTR).

8.  Greifen Sie mit dem **Feld \_ Offset** auf alle Fenster-und Klassen Daten zu.

    Es ist üblich, mithilfe von hart codierten Offsets auf Fenster Daten zuzugreifen. Dieses Verfahren ist nicht für 64-Bit-Windows-Anwendungen portabel. Um Ihren Code portabel zu machen, greifen Sie mit dem **Field \_ Offset** -Makro auf die Fenster-und Klassen Daten zu. Gehen Sie nicht davon aus, dass der zweite Zeiger einen Offset von 4 aufweist.

9.  Der **LPARAM**-, der **wParam**-und der **LRESULT** -Typ ändern die Größe mit der-Plattform.

    Beim Kompilieren von 64-Bit-Code werden diese Typen auf 64 Bits erweitert, da Sie in der Regel Zeiger oder ganzzahlige Typen enthalten. Mischen Sie diese Werte nicht mit den Werten **DWORD**, **ulong**, **uint**, **int**, **int** oder **Long** . Überprüfen Sie, wie Sie diese Typen verwenden, und stellen Sie sicher, dass Sie die Werte nicht versehentlich abschneiden.

 

 