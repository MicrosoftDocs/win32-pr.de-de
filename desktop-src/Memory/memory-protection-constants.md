---
Description: 'Im folgenden finden Sie die Speicherschutz Optionen: Sie müssen einen der folgenden Werte angeben, wenn Sie eine Seite im Arbeitsspeicher zuordnen oder schützen. Schutz Attribute können nicht einem Teil einer Seite zugewiesen werden. Sie können nur einer ganzen Seite zugewiesen werden.'
ms.assetid: 09839db7-2118-4a7d-a707-a08c92bd600c
title: Speicherschutz Konstanten (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 641fab68024d9db96f50327f7c78d51f3f9bca01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369973"
---
# <a name="memory-protection-constants"></a>Speicherschutz Konstanten

Im folgenden finden Sie die Speicherschutz Optionen: Sie müssen einen der folgenden Werte angeben, wenn Sie eine Seite im Arbeitsspeicher zuordnen oder schützen. Schutz Attribute können nicht einem Teil einer Seite zugewiesen werden. Sie können nur einer ganzen Seite zugewiesen werden.

## <a name="example"></a>Beispiel

```cpp
STDMETHODIMP CExtBuffer::FInit
    (
    ULONG cItemMax,     //@parm IN | Maximum number of items ever
    ULONG cbItem,       //@parm IN | Size of each item, in bytes
    ULONG cbPage        //@parm IN | Size of system page size (from SysInfo)
    )
{
    BYTE  *pb;

    m_cbReserved = ((cbItem *cItemMax) / cbPage + 1) *cbPage;
    m_rgItem = (BYTE *) VirtualAlloc( NULL, m_cbReserved, MEM_RESERVE, PAGE_READWRITE );

    if (m_rgItem == NULL)
        return ResultFromScode( E_OUTOFMEMORY );

    m_cbItem  = cbItem;
    m_dbAlloc = (cbItem / cbPage + 1) *cbPage;
    pb = (BYTE *) VirtualAlloc( m_rgItem, m_dbAlloc, MEM_COMMIT, PAGE_READWRITE );
    if (pb == NULL)
        {
        VirtualFree((VOID *) m_rgItem, 0, MEM_RELEASE );
        m_rgItem = NULL;
        return ResultFromScode( E_OUTOFMEMORY );
        }

    m_cbAlloc = m_dbAlloc;
    return ResultFromScode( S_OK );
}
```
Beispiel: aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/dataaccess/oledb/sampprov/extbuff.cpp) auf GitHub.

## <a name="constants"></a>Konstanten


| Konstante/Wert                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_EXECUTE"></span><span id="page_execute"></span><dl> <dt>**Seite \_**</dt> <dt>0x10</dt> ausführen </dl>                                       | Ermöglicht die Ausführung des Zugriffs auf den zugegebenen Seitenbereich. Der Versuch, in den zugesicherte Bereich zu schreiben, führt zu einer Zugriffsverletzung.<br/> Dieses Flag wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="PAGE_EXECUTE_READ"></span><span id="page_execute_read"></span><dl> <dt>**Seite \_ \_Read**</dt> <dt>0x20</dt> ausführen </dl>                       | Aktiviert den Ausführungs-oder schreibgeschützten Zugriff auf den zugegebenen Bereich von Seiten. Der Versuch, in den zugesicherte Bereich zu schreiben, führt zu einer Zugriffsverletzung.<br/> **Windows Server 2003 und Windows XP:** Dieses Attribut wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " erst nach Windows XP mit SP2 und Windows Server 2003 mit SP1 unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="PAGE_EXECUTE_READWRITE"></span><span id="page_execute_readwrite"></span><dl> <dt>**Seite \_ \_Lese schreiben**</dt> <dt>0x40</dt> ausführen </dl>        | Aktiviert den Ausführungs-, Lese-oder Lese-/Schreibzugriff auf den zugesicherte Seitenbereich.<br/> **Windows Server 2003 und Windows XP:** Dieses Attribut wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " erst nach Windows XP mit SP2 und Windows Server 2003 mit SP1 unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="PAGE_EXECUTE_WRITECOPY"></span><span id="page_execute_writecopy"></span><dl> <dt>**Seite \_ \_Write Copy**</dt> <dt>0x80</dt> ausführen </dl>        | Aktiviert den Ausführungs-, Lese-oder schreibgeschützten Zugriff auf eine zugeordnete Ansicht eines Datei Zuordnungsobjekts. Der Versuch, in eine schreibgeschützte Seite mit Lese-/Schreibzugriff zu schreiben, führt zu einer privaten Kopie der Seite, die für den Prozess erstellt wird. Die Seite "private" ist als " **Seite ausführen"- \_ \_ Lese schreiben** gekennzeichnet, und die Änderung wird auf die neue Seite geschrieben.<br/> Dieses Flag wird von den Funktionen [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**virtualzuordcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) nicht unterstützt. **Windows Vista, Windows Server 2003 und Windows XP:** Dieses Attribut wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.<br/> <br/> |
| <span id="PAGE_NOACCESS"></span><span id="page_noaccess"></span><dl> <dt>**Seite \_ NoAccess**</dt> <dt>0x01</dt> </dl>                                    | Deaktiviert den gesamten Zugriff auf den Seitenbereich, für den ein Commit ausgeführt wurde. Der Versuch, den zugesicherte Bereich zu lesen, zu schreiben oder auszuführen, führt zu einer Zugriffsverletzung.<br/> Dieses Flag wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="PAGE_READONLY"></span><span id="page_readonly"></span><dl> <dt>**Seite \_**</dt>Schreibgeschützt <dt>0x02</dt> </dl>                                    | Ermöglicht den schreibgeschützten Zugriff auf den Seitenbereich, für den ein Commit ausgeführt wurde. Der Versuch, in den zugesicherte Bereich zu schreiben, führt zu einer Zugriffsverletzung. Wenn die [Daten Ausführungs Verhinderung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der zugesicherte Region auszuführen, zu einer Zugriffsverletzung.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="PAGE_READWRITE"></span><span id="page_readwrite"></span><dl> <dt>**Seite \_ Schreib**</dt> Vorgang <dt>0x04</dt> </dl>                                 | Aktiviert schreibgeschützten oder Lese-/Schreibzugriff auf den zugesicherte Seitenbereich. Wenn die [Verhinderung von Datenausführung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der zugefassten Region auszuführen, zu einer Zugriffsverletzung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="PAGE_WRITECOPY"></span><span id="page_writecopy"></span><dl> <dt>**Seite \_ Schreibkopie**</dt> <dt>0x08</dt> </dl>                                 | Ermöglicht den schreibgeschützten Zugriff oder den Kopier-/Schreibzugriff auf eine zugeordnete Ansicht eines Datei Zuordnungsobjekts. Der Versuch, in eine schreibgeschützte Seite mit Lese-/Schreibzugriff zu schreiben, führt zu einer privaten Kopie der Seite, die für den Prozess erstellt wird. Die Seite "private" ist als **Seiten \_ Lesevorgang** gekennzeichnet, und die Änderung wird auf die neue Seite geschrieben. Wenn die [Verhinderung von Datenausführung](data-execution-prevention.md) aktiviert ist, führt der Versuch, Code in der zugefassten Region auszuführen, zu einer Zugriffsverletzung.<br/> Dieses Flag wird von den Funktionen [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) oder [**virtualzuordcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) nicht unterstützt.<br/>                                                                               |
| <span id="PAGE_TARGETS_INVALID"></span><span id="page_targets_invalid"></span><dl> <dt>**Seite \_ Ziele \_ ungültige**</dt> <dt>0x40000000</dt> </dl>        | Legt alle Speicherorte auf den Seiten als ungültige Ziele für cfg fest. Wird zusammen mit allen Seitenschutz ausführen verwendet, wie z. b. **Seite \_ Ausführen**, **Seite \_ Execute \_ Read**, **Page \_ Execute \_ lesewrite** und **Page \_ Execute \_ Write tecopy**. Bei allen indirekten Anrufen an Standorten auf diesen Seiten treten keine cfg-Überprüfungen auf, und der Prozess wird beendet. Das Standardverhalten für zugewiesene ausführbare Seiten ist, als gültige callziele für cfg gekennzeichnet zu werden.<br/> Dieses Flag wird von den [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) [**-oder der**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) -Funktion für die Funktion "die Funktion" nicht unterstützt.<br/>                                                                                                              |
| <span id="PAGE_TARGETS_NO_UPDATE"></span><span id="page_targets_no_update"></span><dl> <dt>**Seite \_ Ziele \_ kein \_ Update**</dt> <dt>0x40000000</dt> </dl> | Für Seiten in der Region werden die cfg-Informationen nicht aktualisiert, während der Schutz für [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)geändert wird. Wenn z. b. die Seiten in der Region mithilfe von **\_ \_ ungültigen Seiten Zielen** zugeordnet wurden, werden die ungültigen Informationen beibehalten, während der Seitenschutz geändert wird. Dieses Flag ist nur gültig, wenn der Schutz in einen ausführbaren Typ geändert wird, z. b. " **Seite \_ Ausführen**", " **Seite \_ Execute \_ Read**", " **Page \_ Execute Read \_ Write** " und " **Page \_ Execute \_ Write** Das Standardverhalten für die **VirtualProtect** -Schutz Änderung in eine ausführbare Datei besteht darin, alle Speicherorte als gültige callziele für cfg zu markieren. <br/>                                           |



Die folgenden modifiziererer können zusätzlich zu den in der vorherigen Tabelle bereitgestellten Optionen verwendet werden, sofern nicht anders angegeben.



| Konstante/Wert                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_GUARD"></span><span id="page_guard"></span><dl> <dt>**Seite \_ Wächter**</dt> <dt>0x100</dt> </dl>                      | Seiten in der Region werden zu Wächter Seiten. Wenn Sie versuchen, auf eine Wächter Seite zuzugreifen, löst das System eine **Status \_ Schutz- \_ Seiten \_ Verletzungs** Ausnahme aus und deaktiviert den Status der Guard-Seite. Wächter Seiten fungieren daher als einmalige Zugriffs Alarm. Weitere Informationen finden Sie unter dem Link zum [Erstellen von Schutzseiten](creating-guard-pages.md).<br/> Wenn ein Zugriffs Versuch dazu führt, dass das System den Status der Wächter Seite deaktiviert, übernimmt der zugrunde liegende Seitenschutz.<br/> Wenn bei einem Systemdienst eine Schutz Seiten Ausnahme auftritt, gibt der Dienst in der Regel einen Fehlerstatus Indikator zurück.<br/> Dieser Wert kann nicht mit **Page \_ NoAccess** verwendet werden.<br/> Dieses Flag wird von der Funktion " [**fiatefilemapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) " nicht unterstützt.<br/>                                                                                                                                                                                                                              |
| <span id="PAGE_NOCACHE"></span><span id="page_nocache"></span><dl> <dt>**Seite \_ NoCache**</dt> <dt>0x200</dt> </dl>                | Legt fest, dass alle Seiten nicht zwischengespeichert werden können. Anwendungen sollten dieses Attribut nur dann verwenden, wenn es für ein Gerät explizit erforderlich ist. Die Verwendung der Interlocked-Funktionen mit Arbeitsspeicher, der **sec \_ NoCache** zugeordnet ist, kann zu einer Ausnahme für eine unzulässige **Ausnahme \_ \_** führen.<br/> Das Flag " **Page \_ NoCache** " kann nicht mit den Flags " **Page \_ Guard**", " **Page \_ NoAccess**" oder " **Page \_ Write Combine** " verwendet werden.<br/> Das Flag " **Page \_ NoCache** " kann nur verwendet werden, wenn mit den Funktionen " [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)", " [**virtualbelegcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)" oder " [**virtualbelegcexnuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) " privater Arbeitsspeicher zugeordnet wird. Um den nicht zwischengespeicherten Speicherzugriff für freigegebenen Speicher zu aktivieren, geben Sie beim Aufrufen der [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) -Funktion das **sec- \_ NoCache** -Flag an.<br/>                                                                                                                                                   |
| <span id="PAGE_WRITECOMBINE"></span><span id="page_writecombine"></span><dl> <dt>**Seite \_ Write Combine**</dt> <dt>0x400</dt> </dl> | Legt fest, dass alle Seiten mit dem Schreibvorgang kombiniert werden. <br/> Anwendungen sollten dieses Attribut nur dann verwenden, wenn es für ein Gerät explizit erforderlich ist. Die Verwendung der Interlocked-Funktionen mit Speicher, der als "Write-Combined" zugeordnet ist, kann zu einer Ausnahme wegen einer Ausnahme wegen ungültiger **Ausnahme \_ \_** führen <br/> Das Flag für die **Seiten \_ schreibkombination** kann nicht mit den Flags " **Page \_ NoAccess**", " **Page \_ Guard**" und " **Page \_ NoCache** " angegeben werden. <br/> Das Flag für die **Seiten \_ schreibkombination** kann nur verwendet werden, wenn privater Arbeitsspeicher mit den Funktionen [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**virtualbelegcex**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)oder [**virtualbelegcexnuma zugewiesen**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) wird. Um den Schreib kombinierten Speicherzugriff für freigegebenen Speicher zu aktivieren, geben Sie beim Aufrufen der [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) -Funktion das sec-Flag " **\_ Write-Combine** " an.<br/> **Windows Server 2003 und Windows XP:** Dieses Flag wird erst ab Windows Server 2003 mit SP1 unterstützt.<br/> |



Die folgenden Konstanten können nur mit der [**loadenclavedata**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) -Funktion verwendet werden, wenn Sie eine Enclave angeben, die über die Intel Software Guard Extensions (SGX)-Architektur verfügt.



| Konstante                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PAGE_ENCLAVE_THREAD_CONTROL"></span><span id="page_enclave_thread_control"></span><dl> <dt>**Seiten \_ Enclave- \_ Thread \_ Steuerelement**</dt> </dl> | Die Seite enthält eine Thread Steuerungsstruktur (TCS).<br/>                                                                              |
| <span id="PAGE_ENCLAVE_UNVALIDATED"></span><span id="page_enclave_unvalidated"></span><dl> <dt>**Seiten \_ Enclave \_ nicht validiert**</dt> </dl>           | Der von Ihnen bereitgestellte Seiten Inhalt wird von der Messung mit der eextend-Anweisung des Intel SGX-Programmiermodells ausgeschlossen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)
</dt> <dt>

[Arbeitsspeicherschutz](memory-protection.md)
</dt> <dt>

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
</dt> <dt>

[**Virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)
</dt> <dt>

[**Loadenclavedata**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)
</dt> </dl>

 

 
