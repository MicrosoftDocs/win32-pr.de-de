---
description: Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
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
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104995238"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>Istorageprovidercopyhook:: copycallback-Methode

Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.

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

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das Fenster, das der Kopier-Hook-Handler als übergeordnetes Element für alle Benutzeroberflächen Elemente verwenden soll, die der Handler möglicherweise anzeigen muss. Wenn **FOF_SILENT** im- *Vorgang* angegeben wird, sollte die-Methode diesen Parameter ignorieren.

</dd> </dl>

<dl> <dt>

*Vorgang* \[ in\]
</dt> <dd>

Der auszuführende Vorgang. Dieser Parameter kann einer der Werte sein, die unter dem **wfunc** -Member der [shatleopstruct](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) -Struktur aufgeführt sind.

</dd> </dl>

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Die Flags, die den Vorgang steuern. Bei diesem Parameter kann es sich um einen oder mehrere der Werte handeln, die unter dem *fFlags* -Member der [shatleopstruct](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) -Struktur aufgeführt sind.

Bei druckerkopierhooks ist dieser Wert einer der folgenden Werte, die in "shellapi. h" definiert sind.

| Wert       | BESCHREIBUNG |
|-------------|------------|
|  **PO_DELETE**      | Ein Drucker wird gelöscht. Der *srcfile* -Parameter verweist auf den vollständigen Pfad zum angegebenen Drucker.           |
|  **PO_RENAME**       | Ein Drucker wird umbenannt. Der *srcfile* -Parameter verweist auf den neuen Namen des Druckers. Der *destfile* -Parameter verweist auf den alten Namen.           |
| **PO_PORTCHANGE**    | Wird nicht unterstützt. Darf nicht verwendet werden.          |
| **PO_REN_PORT**    | Wird nicht unterstützt. Darf nicht verwendet werden.           |

</dd> </dl>

<dl> <dt>

*srcfile* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Quell Ordners enthält.

</dd> </dl>

*srcatcher* \[ in\]
</dt> <dd>

Die Attribute des Quell Ordners. Dieser Parameter kann eine Kombination aus beliebigen dateiattributflags (FILE_ATTRIBUTE_ *) sein, die in den Header Dateien definiert sind. Siehe [Datei Attribut Konstanten](../fileio/file-attribute-constants.md).

</dd> </dl>

*destfile* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Ziel Ordners enthält.

</dd> </dl>

"out"  \[ in\]
</dt> <dd>

Die Attribute des Ziel Ordners. Dieser Parameter kann eine Kombination aus beliebigen dateiattributflags (FILE_ATTRIBUTE_ *) sein, die in den Header Dateien definiert sind. Siehe [Datei Attribut Konstanten](../fileio/file-attribute-constants.md).

</dd> </dl>

*Ergebnis* \[ vorgenommen\]
</dt> <dd>

Der ganzzahlige Wert, der angibt, ob die Shell den Vorgang ausführen soll. Einer der folgenden:

| Wert       | BESCHREIBUNG |
|-------------|------------|
| **IDYES**       | Ermöglicht den Vorgang.           |
| **IDNO**        | Verhindert, dass der Vorgang in diesem Ordner erfolgt, aber mit allen anderen Vorgängen, die genehmigt wurden (z. b. einem Batch Kopiervorgang) fortgesetzt wird.           |
| **IDCANCEL**    | Verhindert den aktuellen Vorgang und bricht alle ausstehenden Vorgänge ab.           |


</dd> </dl>


## <a name="return-value"></a>Rückgabewert

Gibt **S_OK** zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Bemerkungen

Die Shell Ruft den Kopier-Hook-Handler des cloudanbieters für jeden Ordner unter dem registrierten Synchronisierungs Stamm auf. Legen Sie zum Registrieren eines kopierhook-Handlers für Cloud-Ordner den **copyhook** -Wert unter dem **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid}** -Schlüssel auf die CLSID des Kopier-Hook-Objekts fest.

Wenn die **copycallback** -Methode aufgerufen wird, initialisiert die Shell die [istorageprovidercopyhook](nn-shobjidl-istorageprovidercopyhook.md) -Schnittstelle direkt, ohne zuerst eine [ishellextinit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle zu verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 Insider Preview-Build 19624                                |
| Header                   | shobjidl. h   |

## <a name="see-also"></a>Weitere Informationen

[Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt](../cfapi/build-a-cloud-file-sync-engine.md)