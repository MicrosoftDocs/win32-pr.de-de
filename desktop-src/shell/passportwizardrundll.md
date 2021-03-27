---
description: Hiermit wird der Passport-Assistent bei der Verwendung mit Rundll32.exe gestartet.
title: Passportwizardrundll-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216606"
---
# <a name="passportwizardrundll-function"></a>Passportwizardrundll-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Hiermit wird der Passport-Assistent bei der Verwendung mit Rundll32.exe gestartet.

## <a name="syntax"></a>Syntax


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndstub* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle für ein Besitzer Fenster. Dieser Parameter ist in der Regel auf **null** festgelegt.

</dd> <dt>

*happinstance* \[ in\]
</dt> <dd>

Typ: **HINSTANCE**

Ein Handle für die Bibliotheksdatei, die als Rückgabewert von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz") abgerufen wird.

</dd> <dt>

*lpszCmdLine* \[ in\]
</dt> <dd>

Typ: **LPTSTR**

Argument Daten. Dieser Wert ist immer leer.

</dd> <dt>

*nCmdShow* \[ in\]
</dt> <dd>

Typ: **int**

Legt den Anzeigemodus für das Fenster fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Der Passport-Assistent wird verwendet, um einen Standard Passport für Windows zu erhalten. Ein Passport ermöglicht dem Benutzer den personalisierten Zugriff auf alle MSN Websites und anderen Passport-fähigen Websites mithilfe der e-Mail-Adresse des Benutzers. Die Verwendung von **passportwizardrundll** als Einstiegspunkt in die Netplwiz.dll Datei über einen rundll32-Befehl ermöglicht es Ihnen, den Passport-Assistenten von einer Befehlszeile aus zu starten, als wäre es eine ausführbare Datei.

**Passportwizardrundll** wird nur im Kontext eines Rundll32.exe Befehls wie folgt verwendet:

**rundll32.exe netplwiz.dll, passportwizardrundll**

Die Verwendung einer Einstiegspunkt Funktion mit Rundll32.exe ähnelt keinem normalen Funktions aufzurufen. Der Funktionsname und der Name der DLL-Datei, in der er gespeichert ist, werden nur als Befehlszeilenparameter verwendet. Die unter Syntax gezeigte Funktionsdefinition ist nur ein Standard Prototyp für alle Funktionen, die Sie mithilfe von rundll32 abrufen können. Die spezifischen Werte für *hwndstub*, *happinstance* und *nCmdShow* werden nicht vom Benutzer bereitgestellt, sondern im Hintergrund durch rundll32 behandelt. **Passportwizardrundll** verwendet nicht den *lpszCmdLine* -Wert, sodass keine zusätzlichen Daten erforderlich sind.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (Version 5,60 oder höher)</dt> </dl> |



 

 
