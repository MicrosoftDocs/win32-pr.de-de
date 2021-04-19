---
title: Funktions Rückgabewerte
description: Funktions Rückgabewerte ähneln "\ out \"-Parametern, da Ihre Daten nicht durch die Client Anwendung bereitgestellt werden.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342372"
---
# <a name="function-return-values"></a>Funktions Rückgabewerte

Funktions Rückgabewerte ähneln reinen **\[ out \]**-Parametern, da Ihre Daten nicht durch die Client Anwendung bereitgestellt werden. Sie werden jedoch anders verwaltet. Im Gegensatz zu reinen **\[ out \]**-Parametern müssen Sie keine Zeiger sein. Die Remote Prozedur kann jeden gültigen Datentyp außer Verweis Zeigern und nicht gekapselten Unions zurückgeben.

Es wird jedoch empfohlen, einen **\[ out \]** -Parameter anstelle eines Rückgabewerts für komplexe Datentypen zu verwenden. Beim zurückgeben komplexer Datentypen generiert der Mittelwert Compiler einen/OS-modusstub. Folglich gehen alle kürzlich von/robust bereitgestellten Fehler Überprüfungs Informationen verloren.

Funktions Rückgabewerte, bei denen es sich um Zeiger Typen handelt, werden vom Clientstub mit einem aufzurufenden [ \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1)Zuordnungs Befehl zugeordnet. Dementsprechend kann nur das Unique-Attribut oder das Full-Zeiger Attribut auf einen Zeiger Funktions Rückgabetyp angewendet werden.

 

 