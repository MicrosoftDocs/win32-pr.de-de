---
description: Versuchen Sie, während des Debuggens weitere Informationen zu Direct3D-Objekten zu erhalten? Der folgende Screenshot zeigt beispielsweise, was in der Regel angezeigt wird, wenn Sie sich eine Direct3D-Schnittstelle im Überwachungsfenster ansehen.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Aktivieren von Direct3D-Debuginformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88851c144c2e651e920d870618f66a38028207bc5503f513f45fb053e16bd2e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730161"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Aktivieren von Direct3D-Debuginformationen (Direct3D 9)

Versuchen Sie, während des Debuggens weitere Informationen zu Direct3D-Objekten zu erhalten? Der folgende Screenshot zeigt beispielsweise, was in der Regel angezeigt wird, wenn Sie sich eine Direct3D-Schnittstelle im Überwachungsfenster ansehen.

![Screenshot einer direct3d-Schnittstelle im Überwachungsfenster](images/d3d-debug-info1.png)

Sie können die Hauptdebuggingobjekte aktivieren, sodass ein gespiegeltes Objekt, das alle Eigenschaften des Objekts enthält, im Überwachungsfenster angezeigt werden kann. Fügen Sie einfach den folgenden \# Define-Code vor der Datei D3D9.h in Ihren Code ein:


```
#define D3D_DEBUG_INFO
```



Um Debuginformationen zu aktivieren, muss die \# Definition vor der Datei D3D9.h erstellt werden (jedes Programm, das DXUT verwendet, aktiviert automatisch D3D DEBUG \_ \_ INFO, wenn das Programm für das Debuggen kompiliert wird). Wenn Sie ein SDK-Beispiel ausführen, sehen Sie dies in DXStdAfx.h (was sich auf alle C++-Beispiele auswirkt). Sie müssen auch die Direct3D-Debuglaufzeit ausführen (die bei Bedarf über die Systemsteuerung aktiviert werden kann).

Hier ist ein Beispiel mit dem [BasicHLSL-Beispiel](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Fügen Sie der \# Datei Dxstdafx.h vor Zeile 37 den Define hinzu.
2.  Erstellen sie ein Debugprojekt.
3.  Festlegen eines Haltepunkts in Zeile 307 in BasicHLSL.cpp
4.  Führen Sie den Debugger aus.

Der folgende Screenshot zeigt die Art detaillierter Informationen, die Sie über ein Direct3D-Texturobjekt aus dem Überwachungsfenster abrufen können.

![Screenshot eines direct3d-Texturobjekts im Überwachungsfenster](images/d3d-debug-info2.png)

> [!Note]
>
> Die Objekteigenschaftennamen sind sichtbar, und die Werte sind nur richtig, wenn die Debuglaufzeit aktiviert ist. Wenn die Ausführung für die Einzelhandelslaufzeit erfolgt, sind die Werte ungültig.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Verwenden der Aufrufliste für erweitertes Debuggen

Wenn Das Direct3D-Debuggen aktiviert ist, können Sie bei jeder Erstellung eines Objekts auch eine Aufrufliste betrachten. Dadurch wird Ihre Anwendung sehr langsam, kann aber verwendet werden, um nach Ressourcenverlusten zu suchen. Legen Sie den folgenden Registrierungsschlüssel auf 1 fest, um die Aufrufliste zu schreiben:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



Wenn Sie Ihre Anwendung mit aktivierten Debuggen erstellen, erhalten Sie Zugriff auf diese zusätzliche Variable:


```
  LPCWSTR CreationCallStack;
```



Diese Variable speichert die Aufrufliste jedes Mal, wenn ein Objekt erstellt wird. Dadurch wird Ihre Anwendung sehr langsam, kann aber zum Debuggen von Ressourcenverlusten verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 



