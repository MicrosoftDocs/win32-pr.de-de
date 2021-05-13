---
description: Startet den Passport-Assistenten bei Verwendung mit Rundll32.exe.
title: PassportWizardRunDll-Funktion
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
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842511"
---
# <a name="passportwizardrundll-function"></a>PassportWizardRunDll-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]

Startet den Passport-Assistenten bei Verwendung mit Rundll32.exe.

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

*hwndStub* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle für ein Besitzerfenster. Dieser Parameter wird in der Regel auf **NULL festgelegt.**

</dd> <dt>

*hAppInstance* \[ In\]
</dt> <dd>

Typ: **HINSTANCE**

Ein Handle für die Bibliotheksdatei, das als Rückgabewert von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz") erhalten wird.

</dd> <dt>

*lpszCmdLine* \[ In\]
</dt> <dd>

Typ: **LPTSTR**

Argumentdaten. Dieser Wert ist immer leer.

</dd> <dt>

*nCmdShow* \[ In\]
</dt> <dd>

Typ: **int**

Legt den Anzeigemodus für das Fenster fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Der Passport-Assistent wird verwendet, um einen Standardpass für Windows zu erhalten. Ein Passport gewährt dem Benutzer personalisierten Zugriff auf alle MSN-Websites und andere Passport-fähige Websites unter Verwendung der E-Mail-Adresse des Benutzers. Wenn Sie **PassportWizardRunDll** als Einstiegspunkt in die Netplwiz.dll-Datei über einen Rundll32-Befehl verwenden, können Sie den Passport-Assistenten über eine Befehlszeile starten, als wäre es eine ausführbare Datei.

**PassportWizardRunDll** wird ausschließlich im Kontext eines Rundll32.exe Befehls wie folgt verwendet:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

Die Verwendung einer Einstiegspunktfunktion mit Rundll32.exe ähnelt keinem normalen Funktionsaufruf. Der Funktionsname und der Name der DLL-Datei, in der sie gespeichert ist, werden nur als Befehlszeilenparameter verwendet. Die unter Syntax gezeigte Funktionsdefinition ist nur ein Standardprototyp für alle Funktionen, die Sie mit Rundll32 aufrufen können. Die spezifischen Werte für *hwndStub,* *hAppInstance* und *nCmdShow* werden nicht vom Benutzer bereitgestellt, sondern im Hintergrund von Rundll32 verarbeitet. **PassportWizardRunDll** verwendet nicht den *LpszCmdLine-Wert, sodass* keine zusätzlichen Daten erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (Version 5.60 oder höher)</dt> </dl> |



 

 
