---
title: Iagentcharacter anzeigen
description: Iagentcharacter anzeigen
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038993"
---
# <a name="iagentcharactershow"></a>Iagentcharacter:: Show

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Zeigt ein Zeichen an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*BFAST*
</dt> <dd>

Statusanimations-Flag wird angezeigt. Wenn dieser Parameter **true** ist, wird die Status Animation **angezeigt** , nachdem das Zeichen sichtbar gemacht wurde. **false** gibt an, dass die Animation nicht wiedergegeben wird.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, [**die die**](/windows/desktop/lwef/iagentcharacter--show) anforderungsanforderungs-ID empfängt.

</dd> </dl>

Vermeiden Sie, den *BFAST* -Parameter auf " **true** " festzulegen, ohne zuvor eine Animation zu spielen. andernfalls wird der Zeichen Rahmen möglicherweise angezeigt, aber es ist kein Bild zum Anzeigen vorhanden. Beachten Sie insbesondere Folgendes: Wenn Sie " [**muveto**](iagentcharacter--moveto.md) " anrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wiedergegeben. Wenn Sie die **Show** -Methode mit *BFAST* auf **true** festlegen, wird daher kein Bild angezeigt. Wenn Sie [**Ausblenden**](/windows/desktop/lwef/iagentcharacter--hide)und dann mit *BFAST* auf **true** festlegen, wird auch kein **Bild angezeigt.**

Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der **Anzeige** Zustands Animation sicherzustellen, bevor Sie diese Methode aufrufen

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: Hide**](iagentcharacter--hide.md)


 

 