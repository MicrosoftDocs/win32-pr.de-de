---
description: Wenn Sie die Eigenschaft ARPNOREMOVE festlegen, wird die Funktion "Software" in der Systemsteuerung deaktiviert, mit der das Produkt entfernt wird.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361914"
---
# <a name="arpnoremove-property"></a>ARPNOREMOVE (Eigenschaft)

Wenn **Sie** die Eigenschaft **ARPNOREMOVE** festlegen, wird die Funktion "Software" in der **Systemsteuerung** deaktiviert, mit der das Produkt entfernt wird. Bei Windows 2000 wird die Schaltfläche **Entfernen** für das **Produkt in der** **Systemsteuerung** unter Software deaktiviert. Bei früheren Betriebssystemen hat dies den Effekt, das Produkt aus der Liste der installierten Produkte in der Systemsteuerung **in der** **Systemsteuerung** zu entfernen.

Wenn die **ARPNOREMOVE** -Eigenschaft festgelegt ist, schreibt die [registerproduct-Aktion](registerproduct-action.md) den Wert "NoRemove" unter den folgenden Registrierungsschlüssel:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**

Wenn Sie die **ARPNOREMOVE** -Eigenschaft festlegen, wird verhindert, dass der UninstallString-Wert unter diesem Schlüssel geschrieben wird. Der unistallstring-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann z. b. während einer Anpassungs Transformation festgelegt werden, um Benutzer daran zu hindern, eine Administrator Anpassung zu entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 oder höher unter Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




