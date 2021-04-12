---
title: Verwenden des System-Supplied Ersatz Zeichens
description: Verwenden des System-Supplied Ersatz Zeichens
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311388"
---
# <a name="using-the-system-supplied-surrogate"></a>Verwenden des System-Supplied Ersatz Zeichens

Wenn Sie das vom System bereitgestellte Ersatz Zeichen für den DLL-Server verwenden möchten, registrieren Sie die dll, indem Sie eine leere Zeichenfolge oder **null** für den Wert [dllersatz](dllsurrogate.md) in der Registrierung angeben. Wenn eine Aktivierungs Anforderung für einen dll-Server, der so festgelegt ist, auf com festgelegt wird, startet com den standardmäßigen Ersatzprozess und die angeforderte DLL (indem er die CLSID intern in der Befehlszeile für den Start angibt), um einen separaten Aufruf zu vermeiden. (Informationen zum Ausführen von mehr als einem DLL-Server in einem Ersatzprozess finden Sie unter [Ersatz für Ersatz](surrogate-sharing.md)Zeichen.)

Die Standard Implementierung des Ersatz Prozesses ist ein Pseudo-com-Server mit gemischtem Threading Modell Stil. Wenn mehrere dll-Server in einen einzelnen Ersatzprozess geladen werden, wird durch diesen Vorgang sichergestellt, dass jeder dll-Server mit dem Threading Modell instanziiert wird, das in der Registrierung für diesen Server angegeben ist. Alle geladenen frei Thread Server werden im Multithread-Apartment vereint, während sich jeder Apartment Thread Server in einem Single Thread-Apartment befindet. Wenn ein dll-Server beide Threading Modelle unterstützt, wählt com das Multithreading.

Dieser Ersatzprozess wird so geschrieben, dass com sowohl das Entladen der DLL-Server als auch das Beenden des Ersatz Vorgangs verarbeitet.

Das vom System bereitgestellte Ersatz Zeichen funktioniert sehr gut für die meisten Entwickler und ist sehr einfach zu verwenden. Allerdings können Entwickler mit besonderen Überlegungen festlegen, dass ein benutzerdefiniertes Ersatz Zeichen erforderlich ist. Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Surrogates](dll-surrogates.md)
</dt> </dl>

 

 




