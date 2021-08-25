---
title: DLL-Serveranforderungen
description: Die meisten DLLs können zwar in einem Ersatzzeichen ausgeführt werden, einige DLLs hingegen nicht.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 624b516f4b6c9deb00e3a093bd3531d3453e631450a1e5ec3b0810569580961a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993240"
---
# <a name="dll-server-requirements"></a>DLL-Serveranforderungen

Die meisten DLLs können zwar in einem Ersatzzeichen ausgeführt werden, einige DLLs hingegen nicht.

Die DLL muss sich gut verhalten, wenn Sie das vom System bereitgestellte Ersatzzeichen verwenden möchten. Beispielsweise würde eine DLL, die Methoden aufruft, die Rückrufe vom Client registrieren, versuchen, diese Rückrufe aufzurufen, als ob die empfangenen Funktionszeiger Anweisungen im Adressraum erhalten hätten, was nicht der Fall wäre. Ebenso funktioniert eine DLL, die eine globale Variable verwendet, die vom Client erwartet wird, nicht. Im Allgemeinen verhindern Parameter, die nicht ordnungsgemäß gemarshallt werden können, die Ausführung des DLL-Servers außerhalb des Clientprozesses. In vielen Fällen können Sie ein benutzerdefiniertes Ersatzzeichen schreiben, das speziell entwickelt wurde, um "schlechtes" Verhalten zu kompensieren. (Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatzzeichens.)](writing-a-custom-surrogate.md)

Wenn der DLL-Server benutzerdefinierte Schnittstellen verwendet, müssen Sie sicherstellen, dass Marshallingcode für diese Schnittstellen verfügbar ist. Beispielsweise können Sie eine Proxy-DLL erstellen und registrieren oder eine Typbibliothek bereitstellen und registrieren, die es dem Server ermöglicht, ordnungsgemäß zu funktionieren, während er in einem Ersatzzeichen ausgeführt wird.

DLL-Server werden nur in einen Ersatzprozess geladen, der im richtigen Sicherheitskontext ausgeführt wird. Der Sicherheitskontext für das DLL-Server-Ersatzzeichen wird auf die gleiche Weise wie für EXE-Server bestimmt. Das DLL-Server-Ersatzzeichen wird im gleichen Sicherheitskontext wie der Client ausgeführt, es sei denn, ein **RunAs-Wert,** der den Sicherheitskontext bestimmt, wird im Abschnitt [AppID-Registrierung](appid-clsid.md) für den Server festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Ersatzzeichen](dll-surrogates.md)
</dt> </dl>

 

 




