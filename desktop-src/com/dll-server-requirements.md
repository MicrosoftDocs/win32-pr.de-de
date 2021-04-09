---
title: DLL-Server Anforderungen
description: Obwohl die meisten DLLs in einem Ersatz Zeichen ausgeführt werden können, können einige DLLs nicht.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037616"
---
# <a name="dll-server-requirements"></a>DLL-Server Anforderungen

Obwohl die meisten DLLs in einem Ersatz Zeichen ausgeführt werden können, können einige DLLs nicht.

Die dll muss sich gut Verhalten, wenn Sie das vom System bereitgestellte Ersatz Zeichen verwenden möchten. Beispielsweise würde eine DLL, die Methoden aufruft, die Rückrufe vom Client registrieren, versuchen, diese Rückrufe so aufzurufen, als ob die Funktionszeiger, die Sie erhalten hat, Anweisungen in ihrem Adressraum hätten, was nicht der Fall ist. Ebenso funktioniert eine DLL, die eine globale Variable verwendet, auf die der Client zugreift, nicht. Im Allgemeinen verhindern Parameter, die nicht ordnungsgemäß gemarshallt werden können, dass der DLL-Server außerhalb des Client Prozesses ausgeführt wird. In vielen Fällen können Sie ein benutzerdefiniertes Ersatz Zeichen schreiben, das speziell so entworfen wurde, dass es das "schlechte" Verhalten kompensiert. (Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens.)

Wenn der DLL-Server benutzerdefinierte Schnittstellen verwendet, müssen Sie sicherstellen, dass Marshalling-Code für diese Schnittstellen verfügbar ist. Beispielsweise können Sie eine Proxy-dll erstellen und registrieren oder eine Typbibliothek bereitstellen und registrieren, die es dem Server ermöglicht, bei Ausführung in einem Ersatz Zeichen ordnungsgemäß zu funktionieren.

DLL-Server werden nur in einen Ersatzprozess geladen, der im richtigen Sicherheitskontext ausgeführt wird. Der Sicherheitskontext für den DLL-Server Ersatz wird auf die gleiche Weise wie für exe-Server bestimmt. Das dll-Server-Ersatz Zeichen wird im gleichen Sicherheitskontext wie der Client ausgeführt, es sei denn, ein **runas** -Wert, der den Sicherheitskontext bestimmt, wird im [AppID](appid-clsid.md) -Registrierungs Abschnitt für den Server festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Surrogates](dll-surrogates.md)
</dt> </dl>

 

 




