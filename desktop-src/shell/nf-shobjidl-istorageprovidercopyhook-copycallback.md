---
description: Bestimmt, ob die Shell einen Ordner im Synchronisierungsstamm eines Cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 26fe9079e7fdf53809f8c0763fa38f271536f1339d16647936fb141f8d213be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677978"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>IStorageProviderCopyHook::CopyCallback-Methode

Bestimmt, ob die Shell einen Ordner im Synchronisierungsstamm eines Cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.

## <a name="syntax"></a>Syntax

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Ein Handle für das Fenster, das der Kopierhookhandler als übergeordnetes Element für alle Benutzeroberflächenelemente verwenden soll, die der Handler möglicherweise anzeigen muss. Wenn **FOF_SILENT** Vorgang angegeben *wird,* sollte die Methode diesen Parameter ignorieren.

</dd> </dl>

<dl> <dt>

*operation* \[ In\]
</dt> <dd>

Der auszuführende Vorgang. Dieser Parameter kann einer der Werte sein, die unter dem **wFunc-Member** der [SHFILEOPSTRUCT-Struktur aufgeführt](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) sind.

</dd> </dl>

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Die Flags, die den Vorgang steuern. Dieser Parameter kann mindestens einer der Werte sein, die unter dem *fFlags-Member* der [SHFILEOPSTRUCT-Struktur aufgeführt](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) sind.

Für Druckerkopierhooks ist dieser Wert einer der folgenden Werte, die in shellapi.h definiert sind.

| Wert       | BESCHREIBUNG |
|-------------|------------|
|  **PO_DELETE**      | Ein Drucker wird gelöscht. Der *Parameter srcFile* zeigt auf den vollständigen Pfad zum angegebenen Drucker.           |
|  **PO_RENAME**       | Ein Drucker wird umbenannt. Der *Parameter srcFile* zeigt auf den neuen Namen des Druckers. Der *destFile-Parameter* verweist auf den alten Namen.           |
| **PO_PORTCHANGE**    | Wird nicht unterstützt. Darf nicht verwendet werden.          |
| **PO_REN_PORT**    | Wird nicht unterstützt. Darf nicht verwendet werden.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Quellordners enthält.

</dd> </dl>

*srcAttribs* \[ In\]
</dt> <dd>

Die Attribute des Quellordners. Dieser Parameter kann eine Kombination aller Dateiattributflags (FILE_ATTRIBUTE_*) sein, die in den Headerdateien definiert sind. Weitere Informationen [finden Sie unter Dateiattributkonst konstanten](../fileio/file-attribute-constants.md).

</dd> </dl>

*destFile* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Zielordners enthält.

</dd> </dl>

*destAttribs* \[ In\]
</dt> <dd>

Die Attribute des Zielordners. Dieser Parameter kann eine Kombination aller Dateiattributflags (FILE_ATTRIBUTE_*) sein, die in den Headerdateien definiert sind. Weitere Informationen [finden Sie unter Dateiattributkonst konstanten](../fileio/file-attribute-constants.md).

</dd> </dl>

*Ergebnis* \[ out\]
</dt> <dd>

Der ganzzahlige Wert, der angibt, ob die Shell den Vorgang ausführen soll. Einer der folgenden:

| Wert       | BESCHREIBUNG |
|-------------|------------|
| **IDYES**       | Lässt den Vorgang zu.           |
| **IDNO**        | Verhindert den Vorgang für diesen Ordner, setzt aber alle anderen Vorgänge fort, die genehmigt wurden (z. B. ein Batchkopiervorgang).           |
| **IDCANCEL**    | Verhindert den aktuellen Vorgang und bricht alle ausstehenden Vorgänge ab.           |


</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt **S_OK,** wenn erfolgreich, oder andernfalls einen Fehlercode zurück.

## <a name="remarks"></a>Hinweise

Die Shell ruft den Copy Hook-Handler des Cloudanbieters für jeden Ordner unter dem registrierten Synchronisierungsstamm auf. Um einen Copy Hook-Handler für Cloudordner zu registrieren, legen Sie den **CopyHook-Wert** unter dem Schlüssel **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** auf die CLSID des Kopierhookobjekts fest.

Wenn die **CopyCallback-Methode** aufgerufen wird, initialisiert die Shell die [IStorageProviderCopyHook-Schnittstelle](nn-shobjidl-istorageprovidercopyhook.md) direkt, ohne zuerst eine [IShellExtInit-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) zu verwenden.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 Insider Preview Build 19624                                |
| Header                   | shobjidl.h   |

## <a name="see-also"></a>Weitere Informationen

[Erstellen einer Cloudsynchronisierungs-Engine, die Platzhalterdateien unterstützt](../cfapi/build-a-cloud-file-sync-engine.md)