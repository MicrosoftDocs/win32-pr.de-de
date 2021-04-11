---
description: Versuchen Sie, während des Debuggens Weitere Informationen über Direct3D-Objekte zu erhalten? Der folgende Screenshot zeigt beispielsweise, was Sie in der Regel sehen, wenn Sie eine Direct3D-Schnittstelle im Überwachungs Fenster sehen.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Aktivieren von Direct3D-Debuginformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123355"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Aktivieren von Direct3D-Debuginformationen (Direct3D 9)

Versuchen Sie, während des Debuggens Weitere Informationen über Direct3D-Objekte zu erhalten? Der folgende Screenshot zeigt beispielsweise, was Sie in der Regel sehen, wenn Sie eine Direct3D-Schnittstelle im Überwachungs Fenster sehen.

![Screenshot einer Direct3D-Schnittstelle im Fenster "überwachen"](images/d3d-debug-info1.png)

Sie können die kerndebugobjekte aktivieren, sodass ein gespiegeltes Objekt, das alle Eigenschaften des-Objekts enthält, im Überwachungs Fenster angezeigt werden kann. Fügen Sie einfach die folgende \# Definition in Ihren Code vor der Datei d3d9. h ein:


```
#define D3D_DEBUG_INFO
```



Um Debuginformationen zu aktivieren, \# muss die Definition vor der Datei d3d9. h erstellt werden (jedes Programm, das dxut verwendet, aktiviert automatisch D3D- \_ Debuginformationen, \_ Wenn das Programm für das Debuggen kompiliert wird). Wenn Sie ein SDK-Beispiel ausführen, können Sie dies in "dxstdafx. h" sehen (was sich auf alle C++-Beispiele auswirkt). Sie müssen auch die Debug Direct3D Runtime ausführen (die bei Bedarf über die Systemsteuerung aktiviert werden kann).

Im folgenden finden Sie ein Beispiel für die Verwendung des [basichlsl](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)-Beispiels.

1.  Fügen Sie die \# Definition der Datei "dxstdafx. h" vor Zeile 37 hinzu.
2.  Erstellen Sie ein debugprojekt.
3.  Festlegen eines Breakpoints in Zeile 307 in basichlsl. cpp
4.  Führen Sie den Debugger aus.

Der folgende Screenshot zeigt die Art detaillierter Informationen, die Sie über ein Direct3D-Textur Objekt aus dem Fenster Überwachen erhalten können.

![Screenshot eines Direct3D-Textur Objekts im Fenster "überwachen"](images/d3d-debug-info2.png)

> [!Note]
>
> Die Objekt Eigenschaftsnamen sind sichtbar, und die Werte sind nur dann korrekt, wenn die Debug-Laufzeit aktiviert ist. Bei der Ausführung für die Einzelhandels Laufzeit sind die Werte ungültig.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Verwenden der aufrufsstapel für erweitertes Debuggen

Wenn Direct3D Debug aktiviert ist, können Sie sich auch bei jeder Erstellung eines Objekts einen Aufruf Stapel ansehen. Dadurch wird die Anwendung sehr langsam, kann jedoch verwendet werden, um nach Ressourcenverlusten zu suchen. Legen Sie den folgenden Registrierungsschlüssel auf 1 fest, um die-aufrufsstapel zu schreiben:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



Wenn Sie Ihre Anwendung mit aktiviertem Debuggen entwickeln, erhalten Sie Zugriff auf diese zusätzliche Variable:


```
  LPCWSTR CreationCallStack;
```



Diese Variable speichert die Aufruf Stapel jedes Mal, wenn ein Objekt erstellt wird. Dadurch wird die Anwendung sehr langsam, kann jedoch zum Debuggen von Ressourcenverlusten verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 



